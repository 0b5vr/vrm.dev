---
title: "APIの変更履歴"
date: 2018-05-21T10:00:00+09:00
aliases: ["/dev/univrm-0.xx/programming/univrm_api_history/"]
weight: 1
tags: ["api"]
---

## v0.68 ImporterContext の整理

[ランタイムインポーター]({{< relref "runtime_import.md" >}})

## v0.63.2 gltf の extension の実装方法を変更

[how_to_impl_extension]({{< relref "how_to_impl_extension.md" >}})

## v0.56 BlendShapeKey の仕様変更

[BlendShapeKeyのインタフェースを厳格化、整理](https://github.com/vrm-c/UniVRM/wiki/ReleaseNote-v0.56.0%28ja%29#blendshapekey%E3%81%AE%E3%82%A4%E3%83%B3%E3%82%BF%E3%83%95%E3%82%A7%E3%83%BC%E3%82%B9%E3%82%92%E5%8E%B3%E6%A0%BC%E5%8C%96%E6%95%B4%E7%90%86)

## v0.36

### テクスチャ名の格納位置の修正

GLTFの仕様に準拠しました。

* extraはextrasの間違い
* imageはnameを持っていた

```json
json.images[i].extra.name
```

変更後

```json
json.images[i].name
```

### ブレンドシェイプ名の格納位置の修正

GLTFの仕様に準拠しました。

* extraはextrasの間違い
* targetにextrasは不許可
* https://github.com/KhronosGroup/glTF/issues/1036#issuecomment-314078356 

```json
json.meshes[i].primitives[j].targets[k].extra.name
```

変更後

```json
json.meshes[i].primitives[j].extras.targetNames[k]
```
