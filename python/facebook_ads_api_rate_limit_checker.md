# Check the rate limit in Facebook Ads API

```python
def find_between(s, first, last):
    try:
        start = s.index(first) + len(first)
        end = s.index(last, start)
        return s[start:end]
    except ValueError:
        return ""


def check_rate_limit(response, *args, **kwargs):
    call = float(
        find_between(response.headers["x-business-use-case-usage"], 'call_count":', ",")
    )
    cpu = float(
        find_between(
            response.headers["x-business-use-case-usage"], 'total_cputime":', ","
        )
    )
    total = float(
        find_between(response.headers["x-business-use-case-usage"], 'total_time":', ",")
    )
    time_to_regain_access = float(
        find_between(
            response.headers["x-business-use-case-usage"],
            'estimated_time_to_regain_access":',
            "}",
        )
    )
    usage = max(call, cpu, total)
    if time_to_regain_access > 0:
        time.sleep(time_to_regain_access)
    elif usage > 75:
        print("75% Rate Limit Reached. Cooling Time 5 Minutes.")
        time.sleep(300)


session = FacebookSession(
    app_id=APP_ID, app_secret=APP_SECRET, access_token=ACCESS_TOKEN
)
session.requests.hooks["response"].append(check_rate_limit)
api = FacebookAdsApi(session)
FacebookAdsApi.set_default_api(api)

```