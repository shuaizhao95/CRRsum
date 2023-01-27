# CRRsum（中文放射学报告摘要生成数据集）
CRRsum是我们文章中创建中文放射学报告摘要生成数据集，为了中文放射学报告摘要生成任务提供数据集、基准。

```
数据量：训练集(8,136)，验证集(901)，测试集(1,029)
示例：
{
    title: 国鼻骨左侧支粉碎性骨折伴邻近软组织肿胀、异物。部分副鼻窦炎。两肺尖磨玻璃小结节，建议3个月CT复查。两下肺少许索条影。主动脉壁钙化。左肾囊肿。头颅CT平扫颅内未见明显外伤性改变。
    content: 鼻骨左侧支可见骨折线影，断端可见移位，邻近软组织肿胀伴多发点状致密影。两侧颧弓及眼眶壁完整，未见明显骨折线影，眼球壁完整，球内及球后未见异常密度影。部分副鼻窦粘膜增厚。两肺尖(Im13)见磨玻璃小结节，边缘清晰，较大者直径约6mm;两下肺见少许索条影，边缘清晰，余两肺实质内未见明显异常密度影。气管、支气管通畅。纵隔内未见明显肿大淋巴结影。心影大小形态未见明显异常，主动脉壁见钙化。两侧胸腔未见积液。左肾内见小圆形低密度影。脑实质内未见明显异常密度影。脑室系统、脑池及脑沟未见明显异常改变。中线结构居中。颅骨未见明显骨折线影。

}
```

# 数据集划分

```
import json

def data_load(filepath):
    data = []
    temp = []
    with open(filepath, encoding='utf-8') as f:
        d = json.load(f)
        data.append(d)
    for i in data:
        for n in i:
            temp.append((n[1],n[0]))
    return temp
train_data = data_load(r'train.json')
dev_data = data_load(r'dev.json')
test_data = data_load(r'test.json')
``` 
# 实验结果

Waiting...
