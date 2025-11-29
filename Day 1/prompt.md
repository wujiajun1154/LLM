# prompt模板
## 文本概括
```json
[
  {"role": "system",
   "content": "you are helper"},
  {"role": "user",
   "content": "Explain antibiotics\nA:"}
]
```
### 输出结果会类似：
```json
[
  {"role": "assistant",
   "content": "Antibiotics are a type of medication used to treat bacterial infections. They work by either killing the bacteria or preventing them from reproducing, allowing the body’s immune system to fight off the infection. Antibiotics are usually taken orally in the form of pills, capsules, or liquid solutions, or sometimes administered intravenously. They are not effective against viral infections, and using them inappropriately can lead to antibiotic resistance."},
]
```
#### "A:" 是一种在问答中使用的显式提示格式，你在这里使用它是为了告诉模型接下来你期望有一个答案。

```json
[
  {"role": "user",
   "content": "Antibiotics are a type of medication used to treat bacterial infections. They work by either killing the bacteria or preventing them from reproducing, allowing the body’s immune system to fight off the infection. Antibiotics are usually taken orally in the form of pills, capsules, or liquid solutions, or sometimes administered intravenously. They are not effective against viral infections, and using them inappropriately can lead to antibiotic resistance.\nExplain the above in one sentence:"}
]
```
####  用一句话概括
### 输出结果会类似：
```json
[
  {"role": "assistant",
   "content": "Antibiotics are medications that kill bacteria or stop their reproduction to help the immune system fight bacterial infections, but they don't work against viruses and misuse can cause antibiotic resistance."},
]
```
## 信息提取
```json
[
  {"role": "system", "content": "从文本中提取姓名、年龄，返回 {\"name\":\"\",\"age\":0}，不要解释。"},
  {"role": "user", "content": "张三今年25岁。"},
  {"role": "assistant", "content": "{\"name\":\"张三\",\"age\":25}"}
]
```
