## 奇怪的知识增加了

```python
import warnings
warnings.filterwarnings('ignore') # Deleting of the warnings which we are not be interested in
```

## Pandas专栏

* pd.concat():就像数据库的表连接一样有inner join 和out join
  * https://blog.csdn.net/weixin_47661174/article/details/124698328

* df.value_counts()
  * https://blog.csdn.net/weixin_44025103/article/details/125044757
* df.plot.pie():对pd.Series数据画饼图
  * https://www.gairuo.com/p/pandas-plot-pie

* df.crosstab():挖掘colunms之间的关系，联合多列一起统计次数
  * https://blog.csdn.net/yasuowjh/article/details/105691229
* df.groupby():df_train.groupby("Pclass")[["Survived"]].sum()看看满足Pclass的基础上的存活个数
* sns.countplot():画柱状图，可以建立三者关系，x,y,hue
  * https://blog.csdn.net/weixin_44025103/article/details/124894507

* pd.set_option():可以设置pandas列表显示的参数
  * https://blog.csdn.net/weixin_45698190/article/details/106422215

* df.query(): 可以把pandas当成sql语句一样使用

