---
title: 🚧Expression
weight: 30
---

表情周りの操作方法。

> VRM-1.0 の `BlendShapeProxy` は、`VRM10Controller.Expression` になります。

VRM-0.X の例

```cs
void SetExpression(GameObject root)
{
    var controller = root.GetComponent<BlendShapeProxy>();
}
```

VRM-1.0 の例

```cs
void SetExpression(GameObject root)
{
    var controller = root.GetComponent<VRM10Controller>();
}
```
