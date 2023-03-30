1.
```
{
    "name": "audience_orders",
    "aggregation_type": "sum",
    "type": "raw",
    "label": "audience_orders",
    "source": "audience_metrics",
}
```

```
{
    "name": "audience_visitors",
    "aggregation_type": "sum",
    "type": "raw",
    "label": "audience_visitors",
    "source": "audience_metrics",
}
```
```
{
    "name": "audience_visits",
    "aggregation_type": "sum",
    "type": "raw",
    "label": "audience_visits",
    "source": "audience_metrics",
}
```
```
{
    "name": "audience_buy_value",
    "aggregation_type": "sum",
    "type": "raw",
    "label": "audience_buy_value",
    "source": "audience_metrics",
}
```
```
{
    "name": "audience_revenue_per_visitor",
    "aggregation_type": "ratio_type",
    "type": "derived",
    "numerator": {"name": "audience_buy_value", "type": "raw"},
    "denominator": {"name": "audience_visitors", "type": "raw"},
    "label": "audience_revenue_per_visitor",
    "source": "audience_metrics",
}
```
```
{
    "name": "audience_conversion_rate",
    "aggregation_type": "percentage_type",
    "type": "derived",
    "numerator": {"name": "audience_orders", "type": "raw"},
    "denominator": {"name": "audience_visits", "type": "raw"},
    "label": "audience_conversion_rate",
    "source": "audience_metrics",
}
```
```
{
    "name": "audience_aov",
    "aggregation_type": "ratio_type",
    "type": "derived",
    "numerator": {"name": "audience_buy_value", "type": "raw"},
    "denominator": {"name": "audience_orders", "type": "raw"},
    "label": "audience_aov",
    "source": "audience_metrics",
}
```
