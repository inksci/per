# per
PER(Prioritized Experience Replay) implementation in PyTorch

## 2

Add files via upload: cartpole_per.ipynb

- 目录不存在则创建
- bool_break 替换 sys.exit()

## 1

解决由于数据精度限制造成计算误差所带来的空值采样，如果采样为空值，则重新采样。

相关代码：
```
        # last one -- ai@inksci.com
        i = n-1
        data = 0
        while data==0:
            # 重新采样
            s = random.uniform(a, b)
            (idx, p, data) = self.tree.get(s)
        priorities.append(p)
        batch.append(data)
        idxs.append(idx)
```
