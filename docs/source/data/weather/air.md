## [AkShare](https://github.com/jindaxiang/akshare) 另类数据

### 空气-河北

#### 日出和日落-天
接口: air_hebei

目标地址: http://110.249.223.67/publish/

描述: 获取河北省近6天空气污染情况

限量: 单次返回 6 天的数据

输入参数

| 名称   | 类型 | 必选 | 描述                                                                              |
| -------- | ---- | ---- | --- |
| city | str | Y | city="定州市" |


输出参数

| 名称          | 类型 | 默认显示 | 描述           |
| --------------- | ----- | -------- | ---------------- |
| 城市      | str   | Y        | 城市-索引  |
| Datadate      | str   | Y        | 日期  |
| Pollutant      | float   | Y        | PM2.5   |
| MinAQI     | str   | Y        | 最小  |
| MaxAQI      | float   | Y        | 最大   |
| Level      | str   | Y        | 程度  |

接口示例

```python
import akshare as ak
air_df = ak.air_hebei(city="定州市")
print(air_df)
```

数据示例

```
               Datadate Pollutant MinAQI MaxAQI  Level
定州市  2019/11/27 0:00:00     PM2.5     80    110   良-轻度
定州市  2019/11/28 0:00:00     PM2.5     90    120   良-轻度
定州市  2019/11/29 0:00:00     PM2.5    175    205  中度-重度
定州市  2019/11/30 0:00:00     PM2.5    175    205  中度-重度
定州市   2019/12/1 0:00:00     PM2.5    175    205  中度-重度
定州市   2019/12/2 0:00:00     PM2.5     80    110   良-轻度
```