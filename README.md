# Fabric Mod Dev Example
- 修改`gradle.properties` 文件
  - 修改`maven_group` 为你的组织名(类似于Maven中的GroupId)
  - 修改`archives_base_name` 为你的模组名(类似于Maven中的ArtifactId)
  - 修改`minecraft_version` 为你的模组的目标版本(你要为哪个Minecraft版本开发Mod)
  - 修改`yarn_mappings`、`loader_version` 与`fabric_version` 为`minecraft_version` 对应的版本，版本对应关系可在[这里](https://fabricmc.net/versions.html)查看
- 修改`src`目录下的目录名称，对应到你的`maven_group`与`archives_base_name`
- 修改`src/resources/fabric.mod.json`
  - `id` 为你的模组的命名空间
  - `entrypoints.main` 为你的模组的入口(main方法所在类)
  - `mixins` 为`mixins.json` 所在位置
- 修改`<modid>.mixins.json`(modid为你的模组的命名空间, fabric.mod.json中id对应的值)
  - `package` 为mixin所在的包名
  - `client` 为mixin的类名

"mixins"可以从mod.json中删除, 如果你不需要

将所有出现的"modid"字符替换为你自己的modid
