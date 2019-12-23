## [AkShare](https://github.com/jindaxiang/akshare) 另类数据

### 日出和日落

#### 日出和日落-天

接口: weather_daily

目标地址: https://www.timeanddate.com/sun/china/

描述: 获取中国各大城市-日出和日落时间, 数据区间从19990101-至今

限量: 单次返回某一天的数据

输入参数

| 名称   | 类型 | 必选 | 描述                                                                              |
| -------- | ---- | ---- | --- |
| trade_date | str | Y | trade_date="20190801" |
| city | str | Y | city="北京" |

输出参数

| 名称          | 类型 | 默认显示 | 描述           |
| --------------- | ----- | -------- | ---------------- |
| date      | datetime.datetime   | Y        | 日期-索引  |
| Sunrise      | str   | Y        | 日出  |
| Sunset      | float   | Y        | 日落   |
| Daylength-Length      | str   | Y        | -  |
| Daylength-Difference      | float   | Y        | -   |
| Astronomical Twilight-Start      | str   | Y        | -  |
| Astronomical Twilight-End      | float   | Y        | -   |
| Nautical Twilight-Start      | str   | Y        | -  |
| Nautical Twilight-End      | float   | Y        | -   |
| Civil Twilight-Start      | str   | Y        | -  |
| Civil Twilight-End      | float   | Y        | -   |
| Solar Noon-Time      | str   | Y        | -  |
| Solar Noon-Mil. km      | float   | Y        | -   |

接口示例

```python
import akshare as ak
weather_df = ak.weather_daily(trade_date="20190801", city="北京")
print(weather_df)
```

数据示例

```
八月        Sunrise          Sunset  ...  End.2           Time Mil. km
2019-08-01  1  05:12 ↑ (65°)  19:28 ↑ (295°)  ...  19:58  12:20 (68,2°)  151857
```

#### 日出和日落-月

接口: weather_monthly

目标地址: https://www.timeanddate.com/sun/china/

描述: 获取中国各大城市-日出和日落时间, 数据区间从19990101-至今

限量: 单次返回某一月的数据

输入参数

| 名称   | 类型 | 必选 | 描述                                                                              |
| -------- | ---- | ---- | --- |
| trade_date | str | Y | trade_date="20190801" |
| city | str | Y | city="北京" |

输出参数

| 名称          | 类型 | 默认显示 | 描述           |
| --------------- | ----- | -------- | ---------------- |
| date      | datetime.datetime   | Y        | 日期-索引  |
| Sunrise      | str   | Y        | 日出  |
| Sunset      | float   | Y        | 日落   |
| Daylength-Length      | str   | Y        | -  |
| Daylength-Difference      | float   | Y        | -   |
| Astronomical Twilight-Start      | str   | Y        | -  |
| Astronomical Twilight-End      | float   | Y        | -   |
| Nautical Twilight-Start      | str   | Y        | -  |
| Nautical Twilight-End      | float   | Y        | -   |
| Civil Twilight-Start      | str   | Y        | -  |
| Civil Twilight-End      | float   | Y        | -   |
| Solar Noon-Time      | str   | Y        | -  |
| Solar Noon-Mil. km      | float   | Y        | -   |

接口示例

```python
import akshare as ak
weather_df = ak.weather_monthly(trade_date="20190801", city="北京")
print(weather_df)
```

数据示例

```
            八月        Sunrise          Sunset  ...  End.2           Time Mil. km
2019-08-01   1  05:12 ↑ (65°)  19:28 ↑ (295°)  ...  19:58  12:20 (68,2°)  151857
2019-08-01   2  05:13 ↑ (66°)  19:27 ↑ (294°)  ...  19:57  12:20 (67,9°)  151838
2019-08-01   3  05:14 ↑ (66°)  19:26 ↑ (294°)  ...  19:56  12:20 (67,7°)  151818
2019-08-01   4  05:15 ↑ (66°)  19:25 ↑ (293°)  ...  19:55  12:20 (67,4°)  151798
2019-08-01   5  05:16 ↑ (67°)  19:24 ↑ (293°)  ...  19:54  12:20 (67,1°)  151776
2019-08-01   6  05:17 ↑ (67°)  19:23 ↑ (293°)  ...  19:52  12:20 (66,9°)  151754
2019-08-01   7  05:17 ↑ (67°)  19:22 ↑ (292°)  ...  19:51  12:20 (66,6°)  151731
2019-08-01   8  05:18 ↑ (68°)  19:20 ↑ (292°)  ...  19:50  12:20 (66,3°)  151708
2019-08-01   9  05:19 ↑ (68°)  19:19 ↑ (292°)  ...  19:49  12:20 (66,0°)  151684
2019-08-01  10  05:20 ↑ (69°)  19:18 ↑ (291°)  ...  19:47  12:19 (65,7°)  151659
2019-08-01  11  05:21 ↑ (69°)  19:17 ↑ (291°)  ...  19:46  12:19 (65,5°)  151634
2019-08-01  12  05:22 ↑ (69°)  19:15 ↑ (290°)  ...  19:45  12:19 (65,2°)  151608
2019-08-01  13  05:23 ↑ (70°)  19:14 ↑ (290°)  ...  19:43  12:19 (64,9°)  151582
2019-08-01  14  05:24 ↑ (70°)  19:13 ↑ (290°)  ...  19:42  12:19 (64,5°)  151556
2019-08-01  15  05:25 ↑ (71°)  19:11 ↑ (289°)  ...  19:40  12:19 (64,2°)  151529
2019-08-01  16  05:26 ↑ (71°)  19:10 ↑ (289°)  ...  19:39  12:18 (63,9°)  151502
2019-08-01  17  05:27 ↑ (71°)  19:09 ↑ (288°)  ...  19:38  12:18 (63,6°)  151474
2019-08-01  18  05:28 ↑ (72°)  19:07 ↑ (288°)  ...  19:36  12:18 (63,3°)  151446
2019-08-01  19  05:29 ↑ (72°)  19:06 ↑ (287°)  ...  19:35  12:18 (63,0°)  151418
2019-08-01  20  05:30 ↑ (73°)  19:05 ↑ (287°)  ...  19:33  12:17 (62,6°)  151389
2019-08-01  21  05:31 ↑ (73°)  19:03 ↑ (287°)  ...  19:32  12:17 (62,3°)  151360
2019-08-01  22  05:32 ↑ (74°)  19:02 ↑ (286°)  ...  19:30  12:17 (62,0°)  151330
2019-08-01  23  05:33 ↑ (74°)  19:00 ↑ (286°)  ...  19:29  12:17 (61,6°)  151300
2019-08-01  24  05:34 ↑ (74°)  18:59 ↑ (285°)  ...  19:27  12:16 (61,3°)  151270
2019-08-01  25  05:34 ↑ (75°)  18:57 ↑ (285°)  ...  19:25  12:16 (61,0°)  151239
2019-08-01  26  05:35 ↑ (75°)  18:56 ↑ (284°)  ...  19:24  12:16 (60,6°)  151207
2019-08-01  27  05:36 ↑ (76°)  18:54 ↑ (284°)  ...  19:22  12:16 (60,3°)  151175
2019-08-01  28  05:37 ↑ (76°)  18:53 ↑ (283°)  ...  19:21  12:15 (59,9°)  151143
2019-08-01  29  05:38 ↑ (77°)  18:51 ↑ (283°)  ...  19:19  12:15 (59,6°)  151109
2019-08-01  30  05:39 ↑ (77°)  18:50 ↑ (283°)  ...  19:17  12:15 (59,2°)  151075
2019-08-01  31  05:40 ↑ (78°)  18:48 ↑ (282°)  ...  19:16  12:14 (58,9°)  151040
```

### 空气质量-河北

#### 近期空气质量

接口: air_hebei

目标地址: http://110.249.223.67/publish/

描述: 获取河北省近6天空气污染情况

限量: 单次返回 6 天的数据

输入参数

| 名称   | 类型 | 必选 | 描述                                                                              |
| -------- | ---- | ---- | --- |
| city | str | Y | city="定州市"; city="", 则返回所有城市数据 |

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

### 空气质量-全国

#### 空气质量-天

接口: air_city_list

目标地址: https://www.aqistudy.cn/

描述: 获取所有可以获得空气质量数据的城市

限量: 单次返回所有可以获取的城市的字典

输入参数

| 名称   | 类型 | 必选 | 描述                                                                              |
| -------- | ---- | ---- | --- |
| - | - | - | - |


输出参数

| 名称          | 类型 | 默认显示 | 描述           |
| --------------- | ----- | -------- | ---------------- |
| -      | -  | -        | -  |

接口示例

```python
import akshare as ak
air_df = ak.air_city_list()
print(air_df)
```

数据示例

```
{'北京': '北京', '上海': '上海', '广州': '广州', '深圳': '深圳', '杭州': '杭州', '天津': '天津', '成都': '成都', '南京': '南京', '西安': '西安', '武汉': '武汉', '阿坝州': '阿坝州', '安康': '安康', '阿克苏地区': '阿克苏地区', '阿里地区': '阿里地区', '阿拉善盟': '阿拉善盟', '阿勒泰地区': '阿勒泰地区', '安庆': '安庆', '安顺': '安顺', '鞍山': '鞍山', '克孜勒苏州': '克孜勒苏州', '安阳': '安阳', '蚌埠': '蚌埠', '白城': '白城', '保定': '保定', '北海': '北海', '宝鸡': '宝鸡', '毕节': '毕节', '博州': '博州', '白山': '白山', '百色': '百色', '保山': '保山', '白沙': '白沙', '包头': '包头', '保亭': '保亭', '本溪': '本溪', '巴彦淖尔': '巴彦淖尔', '白银': '白银', '巴中': '巴中', '滨州': '滨州', '亳州': '亳州', '长春': '长春', '昌都': '昌都', '常德': '常德', '承德': '承德', '赤峰': '赤峰', '昌吉州': '昌吉州', '五家渠': '五家渠', '昌江': '昌江', '澄迈': '澄迈', '重庆': '重庆', '长沙': '长沙', '常熟': '常熟', '楚雄州': '楚雄州', '朝阳': '朝阳', '沧州': '沧州', '长治': '长治', '常州': '常州', '潮州': '潮州', '郴州': '郴州', '池州': '池州', '崇左': '崇左', '滁州': '滁州', '定安': '定安', '丹东': '丹东', '东方': '东方', '东莞': '东莞', '德宏州': '德宏州', '大理州': '大理州', '大连': '大连', '大庆': '大庆', '大同': '大同', '定西': '定西', '大兴安岭地区': '大兴安岭地区', '德阳': '德阳', '东营': '东营', '黔南州': '黔南州', '达州': '达州', '德州': '德州', '儋州': '儋州', '鄂尔多斯': '鄂尔多斯', '恩施州': '恩施州', '鄂州': '鄂州', '防城港': '防城港', '佛山': '佛山', '抚顺': '抚顺', '阜新': '阜新', '阜阳': '阜阳', '富阳': '富阳', '抚州': '抚州', '福州': '福州', '广安': '广安', '贵港': '贵港', '桂林': '桂林', '果洛州': '果洛州', '甘南州': '甘南州', '固原': '固原', '广元': '广元', '贵阳': '贵阳', '甘孜州': '甘孜州', '赣州': '赣州', '淮安': '淮安', '海北州': '海北州', '鹤壁': '鹤壁', '淮北': '淮北', '河池': '河池', '海东地区': '海东地区', '邯郸': '邯郸', '哈尔滨': '哈尔滨', '合肥': '合肥', '鹤岗': '鹤岗', '黄冈': '黄冈', '黑河': '黑河', '红河州': '红河州', '怀化': '怀化', '呼和浩特': '呼和浩特', '海口': '海口', '呼伦贝尔': '呼伦贝尔', '葫芦岛': '葫芦岛', '哈密地区': '哈密地区', '海门': '海门', '海南州': '海南州', '淮南': '淮南', '黄南州': '黄南州', '衡水': '衡水', '黄山': '黄山', '黄石': '黄石', '和田地区': '和田地区', '海西州': '海西州', '河源': '河源', '衡阳': '衡阳', '汉中': '汉中', '菏泽': '菏泽', '贺州': '贺州', '湖州': '湖州', '惠州': '惠州', '吉安': '吉安', '金昌': '金昌', '晋城': '晋城', '景德镇': '景德镇', '金华': '金华', '西双版纳州': '西双版纳州', '九江': '九江', '吉林': '吉林', '即墨': '即墨', '江门': '江门', '荆门': '荆门', '佳木斯': '佳木斯', '济南': '济南', '济宁': '济宁', '胶南': '胶南', '酒泉': '酒泉', '句容': '句容', '湘西州': '湘西州', '金坛': '金坛', '鸡西': '鸡西', '嘉兴': '嘉兴', '江阴': '江阴', '揭阳': '揭阳', '济源': '济源', '嘉峪关': '嘉峪关', '胶州': '胶州', '焦作': '焦作', '锦州': '锦州', '晋中': '晋中', '荆州': '荆州', '库尔勒': '库尔勒', '开封': '开封', '黔东南州': '黔东南州', '克拉玛依': '克拉玛依', '昆明': '昆明', '喀什地区': '喀什地区', '昆山': '昆山', '临安': '临安', '六安': '六安', '来宾': '来宾', '聊城': '聊城', '临沧': '临沧', '娄底': '娄底', '乐东': '乐东', '廊坊': '廊坊', '临汾': '临汾', '临高': '临高', '漯河': '漯河', '丽江': '丽江', '吕梁': '吕梁', '陇南': '陇南', '六盘水': '六盘水', '拉萨': '拉萨', '乐山': '乐山', '丽水': '丽水', '凉山州': '凉山州', '陵水': '陵水', '莱芜': '莱芜', '莱西': '莱西', '临夏州': '临夏州', '溧阳': '溧阳', '辽阳': '辽阳', '辽源': '辽源', '临沂': '临沂', '龙岩': '龙岩', '洛阳': '洛阳', '连云港': '连云港', '莱州': '莱州', '兰州': '兰州', '林芝': '林芝', '柳州': '柳州', '泸州': '泸州', '马鞍山': '马鞍山', '牡丹江': '牡丹江', '茂名': '茂名', '眉山': '眉山', '绵阳': '绵阳', '梅州': '梅州', '宁波': '宁波', '南昌': '南昌', '南充': '南充', '宁德': '宁德', '内江': '内江', '怒江州': '怒江州', '南宁': '南宁', '南平': '南平', '那曲地区': '那曲地区', '南通': '南通', '南阳': '南阳', '平度': '平度', '平顶山': '平顶山', '普洱': '普洱', '盘锦': '盘锦', '蓬莱': '蓬莱', '平凉': '平凉', '莆田': '莆田', '萍乡': '萍乡', '濮阳': '濮阳', '攀枝花': '攀枝花', '青岛': '青岛', '琼海': '琼海', '秦皇岛': '秦皇岛', '曲靖': '曲靖', '齐齐哈尔': '齐齐哈尔', '七台河': '七台河', '黔西南州': '黔西南州', '清远': '清远', '庆阳': '庆阳', '钦州': '钦州', '衢州': '衢州', '泉州': '泉州', '琼中': '琼中', '荣成': '荣成', '日喀则': '日喀则', '乳山': '乳山', '日照': '日照', '韶关': '韶关', '寿光': '寿光', '绥化': '绥化', '石河子': '石河子', '石家庄': '石家庄', '商洛': '商洛', '三明': '三明', '三门峡': '三门峡', '山南': '山南', '遂宁': '遂宁', '四平': '四平', '商丘': '商丘', '宿迁': '宿迁', '上饶': '上饶', '汕头': '汕头', '汕尾': '汕尾', '绍兴': '绍兴', '三亚': '三亚', '邵阳': '邵阳', '沈阳': '沈阳', '十堰': '十堰', '松原': '松原', '双鸭山': '双鸭山', '朔州': '朔州', '宿州': '宿州', '随州': '随州', '苏州': '苏州', '石嘴山': '石嘴山', '泰安': '泰安', '塔城地区': '塔城地区', '太仓': '太仓', '铜川': '铜川', '屯昌': '屯昌', '通化': '通化', '铁岭': '铁岭', '通辽': '通辽', '铜陵': '铜陵', '吐鲁番地区': '吐鲁番地区', '铜仁地区': '铜仁地区', '唐山': '唐山', '天水': '天水', '太原': '太原', '台州': '台州', '泰州': '泰州', '文昌': '文昌', '文登': '文登', '潍坊': '潍坊', '瓦房店': '瓦房店', '威海': '威海', '乌海': '乌海', '芜湖': '芜湖', '吴江': '吴江', '乌兰察布': '乌兰察布', '乌鲁木齐': '乌鲁木齐', '渭南': '渭南', '万宁': '万宁', '文山州': '文山州', '武威': '武威', '无锡': '无锡', '温州': '温州', '吴忠': '吴忠', '梧州': '梧州', '五指山': '五指山', '兴安盟': '兴安盟', '许昌': '许昌', '宣城': '宣城', '襄阳': '襄阳', '孝感': '孝感', '迪庆州': '迪庆州', '锡林郭勒盟': '锡林郭勒盟', '厦门': '厦门', '西宁': '西宁', '咸宁': '咸宁', '湘潭': '湘潭', '邢台': '邢台', '新乡': '新乡', '咸阳': '咸阳', '新余': '新余', '信阳': '信阳', '忻州': '忻州', '徐州': '徐州', '雅安': '雅安', '延安': '延安', '延边州': '延边州', '宜宾': '宜宾', '盐城': '盐城', '宜昌': '宜昌', '宜春': '宜春', '银川': '银川', '运城': '运城', '伊春': '伊春', '云浮': '云浮', '阳江': '阳江', '营口': '营口', '榆林': '榆林', '玉林': '玉林', '伊犁哈萨克州': '伊犁哈萨克州', '阳泉': '阳泉', '玉树州': '玉树州', '烟台': '烟台', '鹰潭': '鹰潭', '义乌': '义乌', '宜兴': '宜兴', '玉溪': '玉溪', '益阳': '益阳', '岳阳': '岳阳', '扬州': '扬州', '永州': '永州', '淄博': '淄博', '自贡': '自贡', '珠海': '珠海', '湛江': '湛江', '镇江': '镇江', '诸暨': '诸暨', '张家港': '张家港', '张家界': '张家界', '张家口': '张家口', '周口': '周口', '驻马店': '驻马店', '章丘': '章丘', '肇庆': '肇庆', '中山': '中山', '舟山': '舟山', '昭通': '昭通', '中卫': '中卫', '张掖': '张掖', '招远': '招远', '资阳': '资阳', '遵义': '遵义', '枣庄': '枣庄', '漳州': '漳州', '郑州': '郑州', '株洲': '株洲'}
```

#### 空气质量-小时

接口: air_hourly

目标地址: https://www.aqistudy.cn/

描述: 获取具体某一天的每个小时的空气质量数据

限量: 单次返回当天的所有小时的数据

输入参数

| 名称   | 类型 | 必选 | 描述                                                                              |
| -------- | ---- | ---- | --- |
| city | str | Y | city="上海" |
| date | str | Y | date="2019-12-05" |

输出参数

| 名称          | 类型 | 默认显示 | 描述           |
| --------------- | ----- | -------- | ---------------- |
| time      | datetime.datetime   | Y        | 日期时间索引  |
| aqi      | str   | Y        | -  |
| pm2_5      | float   | Y        | PM2.5   |
| pm10     | str   | Y        | PM10  |
| co      | float   | Y        | -   |
| no2      | str   | Y        | -  |
| o3      | str   | Y        | -  |
| so2      | str   | Y        | -  |
| rank      | str   | Y        | -  |

接口示例

```python
import akshare as ak
air_df = ak.air_hourly(city="上海", date="2019-12-05")
print(air_df)
```

数据示例

```
                     aqi pm2_5 pm10   co  no2  o3 so2 rank
time                                                      
2019-12-05 00:00:00  110    83   80  1.0  117   8  13  284
2019-12-05 01:00:00  107    80   75  0.9  115   8  13  276
2019-12-05 02:00:00  104    78   68  0.8  100  14  12  280
2019-12-05 03:00:00   98    73   63  0.7   89  18  12  270
2019-12-05 04:00:00   94    70   63  0.8   91  14  13  264
2019-12-05 05:00:00   95    71   63  0.8   92  10  13  270
2019-12-05 06:00:00   95    71   64  0.8   93   9  12  275
2019-12-05 07:00:00   98    73   70  0.9   99   6  13  275
2019-12-05 08:00:00  102    76   86  1.1  103   7  13  274
2019-12-05 09:00:00  110    83  106  1.0   96  13  13  284
2019-12-05 10:00:00  108    81   78  0.8   62  41  13  277
2019-12-05 11:00:00   87    64   49  0.6   45  59  12  232
2019-12-05 12:00:00   65    47   38  0.5   38  68  11  177
2019-12-05 13:00:00   58    41   34  0.5   36  73  10  163
2019-12-05 14:00:00   53    37   35  0.5   37  76  11  157
2019-12-05 15:00:00   52    36   34  0.4   37  81  12  157
2019-12-05 16:00:00   46    32   34  0.4   35  82  10  131
2019-12-05 17:00:00   49    30   49  0.5   41  76   9  138
2019-12-05 18:00:00   62    44   64  0.7   49  70  10  198
2019-12-05 19:00:00   85    63   69  0.8   54  55  10  242
2019-12-05 20:00:00   85    63   55  0.7   51  56  10  229
2019-12-05 21:00:00   62    44   41  0.5   44  59   8  153
2019-12-05 22:00:00   35    24   21  0.4   34  61   6   39
2019-12-05 23:00:00   22    15   12  0.4   28  63   6   12
```

#### 空气质量-天

接口: air_daily

目标地址: https://www.aqistudy.cn/

描述: 获取从 **start_date** 到 **end_date** 的期间的每天的空气质量数据

限量: 单次返回从 **start_date** 到 **end_date** 的所有天的数据

输入参数

| 名称   | 类型 | 必选 | 描述                                                                              |
| -------- | ---- | ---- | --- |
| city | str | Y | city="上海" |
| start_date | str | Y | start_date="2019-11-01" |
| end_date | str | Y | end_date="2019-12-01" |

输出参数

| 名称          | 类型 | 默认显示 | 描述           |
| --------------- | ----- | -------- | ---------------- |
| time      | datetime.date  | Y        | 日期索引  |
| aqi      | str   | Y        | -  |
| pm2_5      | float   | Y        | PM2.5   |
| pm10     | str   | Y        | PM10  |
| co      | float   | Y        | -   |
| no2      | str   | Y        | -  |
| o3      | str   | Y        | -  |
| so2      | str   | Y        | -  |
| rank      | str   | Y        | -  |

接口示例

```python
import akshare as ak
air_df = ak.air_daily(city="上海", start_date="2019-11-01", end_date="2019-12-01")
print(air_df)
```

数据示例

```
            aqi pm2_5 pm10   co no2   o3 so2 rank
time                                             
2019-11-01   87    42  111  0.7  69  135   9  221
2019-11-02  110    72  146  0.9  60  171   9  231
2019-11-03   55    28   45  0.6  34  106   8  249
2019-11-04   60    32   50  0.7  33  112   8   60
2019-11-05   50    16   30  0.5  36  100   7   18
2019-11-06   58    15   26  0.5  46   90   7   37
2019-11-07   62    32   41  0.7  40  114   8   48
2019-11-08   45    13   29  0.5  29   89   7   42
2019-11-09   54    12   25  0.5  43   92   7   23
2019-11-10   76    39   63  0.7  54  131   9   29
2019-11-11   97    44  103  0.9  77   81  12  201
2019-11-12   70    25   75  0.6  56   72   7  182
2019-11-13   74    54   74  0.9  55   93  10  115
2019-11-14   67    20   84  0.6  38   77   7  162
2019-11-15   60    20   60  0.6  48  108   8  111
2019-11-16   58    22   50  0.5  46  109   9   53
2019-11-17   62    34   60  0.7  49   82   9   64
2019-11-18   84    47  118  0.7  37   63   7  307
2019-11-19   93    33  135  0.6  36   69   9  285
2019-11-20   65    23   79  0.6  49   76   7  138
2019-11-21   62    12   31  0.5  49   62   6   59
2019-11-22   80    26   49  0.5  64   50   9   48
2019-11-23   69    21   37  0.5  55   41   7   40
2019-11-24   50    32   33  0.7  40   62   6   82
2019-11-25   33    13   29  0.4  26   59   5   55
2019-11-26   48    15   26  0.5  38   47   5   63
2019-11-27   44    16   18  0.4  35   49   5   24
2019-11-28   38    16   32  0.5  30   57   6  148
2019-11-29   54    17   32  0.5  43   47   6   89
2019-11-30   73    15   24  0.5  58   38   6   43
2019-12-01   53    27   22  0.9  42   41   5   10
```

#### 空气质量-截面数据

接口: air_all_city

目标地址: https://www.aqistudy.cn/

描述: 获取在 **time_point** 的时间点上所有城市的空气质量数据

限量: 单次返回所有的数据

输入参数

| 名称   | 类型 | 必选 | 描述                                                                              |
| -------- | ---- | ---- | --- |
| period_type | str | Y | period_type="HOUR"; "DAY" or "HOUR" |
| time_point | str | Y | 如果 period_type="HOUR", 则必须设定为 time_point="2019-12-01 20:00:00" 的格式; 如果 period_type="DAY", 则必须设定为 time_point="2019-12-01" 的格式  |

输出参数

| 名称          | 类型 | 默认显示 | 描述           |
| --------------- | ----- | -------- | ---------------- |
| time      | datetime.datetime  | Y        | 日期时间索引  |
| cityname      | str   | Y        | -  |
| cityid      | float   | Y        | PM2.5   |
| latitude     | str   | Y        | PM10  |
| longitude      | float   | Y        | -   |
| aqi      | str   | Y        | -  |
| pm2_5      | str   | Y        | -  |
| pm10      | str   | Y        | -  |
| so2      | str   | Y        | -  |
| no2      | str   | Y        | -  |
| co      | str   | Y        | -  |
| o3      | str   | Y        | -  |
| primary_pollutant      | str   | Y        | -  |

接口示例-HOUR

```python
import akshare as ak
air_df = ak.air_all_city(period_type="HOUR", time_point="2019-12-01 20:00:00")
print(air_df)
```

数据示例-HOUR

```
                    cityname     cityid       latitude       longitude aqi  \
time                                                                         
2019-12-01 20:00:00      七台河  101051002  45.7750050000  131.0190480000  68   
2019-12-01 20:00:00       三亚  101310201  18.2577760000  109.5227710000  34   
2019-12-01 20:00:00       三明  101230801  26.2708350000  117.6421940000  42   
2019-12-01 20:00:00      三门峡  101181701  34.7833200000  111.1812620000  67   
2019-12-01 20:00:00       上海  101020100  31.2491620000  121.4878990000  46   
                      ...        ...            ...             ...  ..   
2019-12-01 20:00:00     黔东南州  101260501  26.6317420000  107.9482390000  36   
2019-12-01 20:00:00      黔南州  101260401  26.1536570000  107.4775590000  27   
2019-12-01 20:00:00     黔西南州  101260901  27.0504130000  106.1208050000  32   
2019-12-01 20:00:00     齐齐哈尔  101050201  47.3477000000  123.9872890000  57   
2019-12-01 20:00:00       龙岩  101230701  25.0786850000  117.0179970000  49   
                    pm2_5 pm10 so2 no2   co  o3 primary_pollutant  
time                                                               
2019-12-01 20:00:00    49   69  12  38  0.9  30             PM2.5  
2019-12-01 20:00:00    12   34   4  14  0.5  64                    
2019-12-01 20:00:00    29   41   9  17  0.8  38                    
2019-12-01 20:00:00    39   83  12  64  1.5  20              PM10  
2019-12-01 20:00:00    32   27   6  45  1.1  20                    
                   ...  ...  ..  ..  ...  ..               ...  
2019-12-01 20:00:00    25   33  30  24  0.8  24                    
2019-12-01 20:00:00    13   22  81  16  0.6  19                    
2019-12-01 20:00:00    22   29   6  25  0.7  18                    
2019-12-01 20:00:00    40   50  39  34  0.6  40             PM2.5  
2019-12-01 20:00:00    34   37   6  17  0.4  41                    
```

接口示例-DAY

```python
import akshare as ak
air_df = ak.air_all_city(period_type="DAY", time_point="2019-12-01")
print(air_df)
```

数据示例-DAY

```
           cityname     cityid       latitude       longitude  aqi pm2_5 pm10  \
time                                                                            
2019-07-21      阿坝州  101271901  31.9057630000  102.2285650000   31    12   20   
2019-07-21    阿克苏地区  101130801  40.3494440000   81.1560130000   81    25  112   
2019-07-21     阿拉善盟  101081201  38.8430750000  105.6956830000   89    16   28   
2019-07-21    阿勒泰地区  101131401  47.8901360000   87.9262140000   55     5   11   
2019-07-21     阿里地区  101140701  30.4045570000   81.1076690000   65     3    8   
             ...        ...            ...             ...  ...   ...  ...   
2019-07-21       富阳  101210108  30.0010940000  119.8466920000    0     0    0   
2019-07-21       苏州  101190401  31.3179870000  120.6199070000  138    34   60   
2019-07-21       伊春  101050801  47.7419590000  128.9005800000   24    12   23   
2019-07-21       玉林  101300901  22.6439740000  110.1516760000   41    18   36   
2019-07-21       济源             35.0672430000  112.6019180000  136    56   86   
           so2 no2   co   o3 primary_pollutant  
time                                            
2019-07-21  11   4  0.2   62                 —  
2019-07-21   6  18  0.4  120          颗粒物:PM10  
2019-07-21   6  10  0.5  146                臭氧  
2019-07-21   7   8  0.5  105                臭氧  
2019-07-21   5  15  0.4  117                臭氧  
         ..  ..  ...  ...               ...  
2019-07-21   0   0  0.0    0                 —  
2019-07-21   4  39  0.6  201                臭氧  
2019-07-21   6   9  0.6   48                 —  
2019-07-21  22  11  0.8   82                 —  
2019-07-21   3  14  1.1  199                O3  
```

### 财富排行榜

接口: fortune_rank

目标地址: http://www.fortunechina.com/fortune500/node_65.htm

描述: 获取指定年份财富世界500强公司排行榜

限量: 单次返回某一个年份的所有历史数据

输入参数

| 名称   | 类型 | 必选 | 描述 |
| -------- | ---- | ---- | --- |
| year | int  | Y    |   year="2019"|

输出参数

| 名称          | 类型 | 默认显示 | 描述           |
| --------------- | ----- | -------- | ---------------- |
| 公司名称      | str   | Y        | -  |
| 营业收入      | float   | Y        | 注意单位   |
| 利润      | float   | Y        | 注意单位   |
| 国家      | float   | Y        | -   |

接口示例

```python
import akshare as ak
fortune_df = ak.fortune_rank(year="2019")
print(fortune_df)
```

数据示例

```
公司名称(中英文)  营业收入(百万美元)  利润(百万美元)   国家
0                             沃尔玛（WALMART)    514405.0    6670.0   美国
1                中国石油化工集团公司（SINOPEC GROUP)    414649.9    5845.0   中国
2            荷兰皇家壳牌石油公司（ROYAL DUTCH SHELL)    396556.0   23352.0   荷兰
3    中国石油天然气集团公司（CHINA NATIONAL PETROLEUM)    392976.6    2270.5   中国
4                       国家电网公司（STATE GRID)    387056.0    8174.8   中国
..                                     ...         ...       ...  ...
495                              纽柯（NUCOR)     25067.3    2360.8   美国
496               蒙特利尔银行（BANK OF MONTREAL)     25002.7    4235.1  加拿大
497        泰康保险集团（TAIKANG INSURANCE GROUP)     24931.7    1794.6   中国
498        Ultrapar控股公司（ULTRAPAR HOLDINGS)     24816.0     314.8   巴西
499                  法国液化空气集团（AIR LIQUIDE)     24796.6    2494.2   法国
```

### 电影票房-实时

接口: movie_board

目标地址: https://maoyan.com/board/1

描述: 获取最新电影的实时票房数据

限量: 将昨日国内热映的影片, 按照昨日票房从高到低排列, 每天上午10点更新

输入参数

| 名称   | 类型 | 必选 | 描述                                                                              |
| -------- | ---- | ---- | --- |
| - | -  | -    |  -|


输出参数

| 名称          | 类型 | 默认显示 | 描述           |
| --------------- | ----- | -------- | ---------------- |
| -     | float   | -        | json返回所有推送数据, 逐步做处理  |  


接口示例

```python
import akshare as ak
movie_df = ak.movie_board()
print(movie_df)
```

数据示例

```
          电影名称                           主演             上映时间          实时票房  \
0           误杀                  主演：肖央,谭卓,陈冲  上映时间：2019-12-13  实时票房:7981.7万   
1          天·火                 主演：王学圻,昆凌,窦骁  上映时间：2019-12-12  实时票房:3569.5万   
2        冰雪奇缘2   主演：克里斯汀·贝尔,伊迪娜·门泽尔,乔纳森·格罗夫  上映时间：2019-11-22  实时票房:1649.3万   
3  勇敢者游戏2：再战巅峰        主演：道恩·强森,凯伦·吉兰,杰克·布莱克  上映时间：2019-12-06  实时票房:1395.1万   
4       被光抓走的人                 主演：黄渤,王珞丹,谭卓  上映时间：2019-12-13  实时票房:1176.2万   
5        我为你牺牲                 主演：李琦,国永振,陈姝  上映时间：2019-12-05  实时票房:1012.7万   
6      南方车站的聚会                 主演：胡歌,桂纶镁,廖凡  上映时间：2019-12-06   实时票房:514.8万   
7         早安公主               主演：田雨,朱颜曼滋,邱雨铄  上映时间：2019-12-13   实时票房:411.0万   
8         唐顿庄园     主演：休·博纳维尔,劳拉·卡尔迈克尔,吉姆·卡特  上映时间：2019-12-13   实时票房:403.3万   
9         利刃出鞘  主演：丹尼尔·克雷格,克里斯·埃文斯,安娜·德·阿玛斯  上映时间：2019-11-29   实时票房:369.6万   
           总票房  
0    总票房:2.25亿  
1    总票房:1.41亿  
2    总票房:7.84亿  
3    总票房:2.69亿  
4  总票房:5894.0万  
5  总票房:4696.0万  
6    总票房:1.95亿  
7  总票房:1170.0万  
8  总票房:1171.0万  
9    总票房:1.92亿  
```

### 生活成本

接口: cost_living

目标地址: https://expatistan.com/cost-of-living/index

描述: 获取世界各大城市生活成本数据

限量: 返回当前时点所有数据

输入参数

| 名称   | 类型 | 必选 | 描述                                                                              |
| -------- | ---- | ---- | --- |
| region     | str   | -        | region="world", 默认, 返回所有城市数据, 其他城市请查看 **城市一览表**  |  

城市一览表

| 名称   | 类型 |   
| -------- | ---- |
| europe | 欧洲  |
| north-america | 北美洲  |
| latin-america | 拉丁美洲  |
| asia | 亚洲  |
| middle-east | 中东  |
| africa | 非洲  |
| oceania | 大洋洲  |
| world | 默认全球所有城市  |

输出参数

| 名称          | 类型 | 默认显示 | 描述           |
| --------------- | ----- | -------- | ---------------- |
| rank     | str   | -        | 排名  |  
| city     | str   | -        | 城市名称 |  
| index    | str   | -        | 价格指数  |  

接口示例

```python
import akshare as ak
cost_df = ak.cost_living()
print(cost_df)
```

数据示例

```
      rank                                       city  index
0      1st              Grand Cayman (Cayman Islands)    271
1      2nd  Mountain View, California (United States)    259
2      3rd      Palo Alto, California (United States)    259
3      4th              New York City (United States)    253
4      5th                       Zurich (Switzerland)    246
..     ...                                        ...    ...
295  296th                             Indore (India)     62
296  297th                             Madras (India)     62
297  298th                        Córdoba (Argentina)     58
298  299th                        Rosario (Argentina)     56
299  300th                        Mendoza (Argentina)     48
```