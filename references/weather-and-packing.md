# 天气与行李清单工作流

## 默认天气信源

默认使用 Open-Meteo Forecast API：

- 官网文档：https://open-meteo.com/en/docs
- 优点：无需 API Key，支持按经纬度查询每日最高/最低温、降水概率、降水量、天气代码、风速等。
- 建议字段：`weather_code,temperature_2m_max,temperature_2m_min,precipitation_probability_max,precipitation_sum,wind_speed_10m_max`
- 查询示例：

```text
https://api.open-meteo.com/v1/forecast?latitude=<lat>&longitude=<lng>&daily=weather_code,temperature_2m_max,temperature_2m_min,precipitation_probability_max,precipitation_sum,wind_speed_10m_max&timezone=Asia%2FShanghai&forecast_days=10
```

## 可靠性规则

- 出行日期在未来 14 天内：可以写入每日天气预报，但要标注来源和查询日期。
- 超过 14 天：不要虚编天气。只写“当前距离出行过远，暂无可靠逐日天气预报；建议出发前 7-10 天刷新”。
- 天气会变，出发前 1-2 天需要再次复核。

## 如何影响规划

- 高降水概率或明显降水量：减少户外散步、江滩、湖边、骑行等；增加博物馆、商场、咖啡馆、室内展览备选。
- 高温：减少中午户外暴晒，安排上午/傍晚户外，中午室内休息。
- 低温或大风：提醒加外套、减少江边长时间停留。

## 行李清单

每次旅行应在地图页最后增加一个“行李”tab。清单不要太长，按类别合并。必须包含用户固定电子/工具物品：

- 电脑、充电器、鼠标、iPad
- 刮胡刀、指甲钳
- 相机

根据天气和目的地特点补充重点项，例如雨伞、防水鞋套、薄外套、防晒、驱蚊、证件、药品等。天气相关或目的地特有物品应加粗或单独列出。
