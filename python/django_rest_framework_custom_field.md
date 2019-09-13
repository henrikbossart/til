# Add custom field to django rest framework serializer

In order to add a custom field (say mapped to a function), use the following:

```python
class SomeSerializer(serializer):
    model: Model
    custom_field = serializers.CharField(source="the_source_function")
    fields = [
        'some_field',
        ...,
        'custom_field'
    ]
```