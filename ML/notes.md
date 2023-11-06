# ML Notes

## Uber

- Converting object to datetime: pd.to_datetime(df["pickup_datetime"])
- df.corr(), to use it before drop the columns which are string such as key
- Plotting a boxplot: plt.boxplot(df["fare_amount"])
- Removing Out-liers

```python
q1 = df["fare_amount"].quantile(0.25)
q3 = df["fare_amount"].quantile(0.75)
# print(q1, q3)
IQR = q3-q1
lwr_bound = q1-(1.5*IQR)
upr_bound = q3+(1.5*IQR)
print(lwr_bound, upr_bound)
```
