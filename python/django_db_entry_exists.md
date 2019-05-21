# Check if a Database entry exists

```python
Object.objects.filter(foo=bar).exists()
```

This will not make a database query, as opposed to using:

```python
if len(Object.objects.filter(foo=bar)) > 0
```