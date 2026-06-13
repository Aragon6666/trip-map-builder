# 2606 Wuhan Research Notes

## Hotel Area

### Recommended Base: 江汉路 / 循礼门 / 江汉关

Reasons:

- D1 晚上可步行覆盖江汉路、江汉关、汉口江滩。
- D2 可跨江去黄鹤楼和粮道街，傍晚轮渡回汉口。
- D3 去省博/东湖虽然跨江，但不需要换酒店。
- D4 去机场可优先走地铁2号线或打车，返程更稳。

Booking filter:

- 近地铁2号线或江汉路核心区。
- 近半年评价重点看卫生、隔音、空调、异味、前台处理。
- 优先可取消房型。
- 候选类型：全季、亚朵、桔子、汉庭优佳等中端/商务连锁，具体门店下单前再查小红书和大众点评差评。

## Attractions

- 黄鹤楼：武汉经典历史地标，适合上午去，端午建议提前看票务/入园规则。
- 江汉关 / 汉口江滩：第一晚轻松夜景，不消耗白天体力。
- 湖北省博物馆：端午避热核心点，建议提前预约；周日安排较稳。
- 东湖听涛 / 梨园：保留湖边散步和拍照，不做高强度绿道骑行。
- 古德寺：最后一天轻量拍照点；若天气热或想减少通勤，替换为黎黄陂路。

## Food Strategy

- 用户不太能吃辣，因此主推荐优先少辣/不辣。
- 武汉小吃选择豆皮、烧麦、汤粉、藕汤、热干面等；点单时明确少辣/不辣。
- 不追网红长队。粮道街、江汉路、汉口老街区只作为“餐饮区域”，现场选择排队少、评价稳的店。
- 大众点评复核关键词：排队久、踩雷、服务差、太辣、游客店、卫生。
- 小红书复核关键词：近期体验、避雷、排队、不辣、情侣、拍照。

## Tooling Notes

- 当前环境未安装 `opencli`，因此未按仓库文档自动抓取大众点评/小红书。
- `trips/2606_wuhan/index.html` 已为地点保留 `xhsKeyword` 和 `dianpingKeyword`，手机端可直接跳转搜索。
- 关键开放时间、预约、票价、轮渡班次仍需出发前一天按官方渠道复核。

## Weather Source

Default source: Open-Meteo Forecast API (`https://open-meteo.com/en/docs`). It does not require an API Key and can return daily temperature, precipitation probability, precipitation sum, weather code, and wind speed by latitude/longitude.

Wuhan query used on 2026-06-14:

```text
https://api.open-meteo.com/v1/forecast?latitude=30.5849&longitude=114.2857&daily=weather_code,temperature_2m_max,temperature_2m_min,precipitation_probability_max,precipitation_sum,wind_speed_10m_max&timezone=Asia%2FShanghai&forecast_days=10
```

Planning impact: 6月19日和6月20日降雨风险较高，因此户外江滩、黄鹤楼、昙华林、轮渡都需要看现场雨势执行；省博、商场、咖啡馆作为雨天缓冲。
