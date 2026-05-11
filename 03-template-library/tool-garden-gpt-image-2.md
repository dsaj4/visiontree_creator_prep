# GPT Image 2 视觉生成工具

- 模板 ID：`tool-garden-gpt-image-2`
- content-system templateId：`tool-garden-gpt-image-2`
- 标签：工具 / 流程
- 来源 Skill：`gpt-image-2`
- 来源版本：`1.0.3`
- 来源链接：<https://github.com/ConardLi/garden-skills/tree/main/skills/gpt-image-2>
- 适合账号：`thinking-lab`、`visiontree`、`thinking-tree`、`nora`、`milo`、`eli`
- 内容类型：图像生成 / 图像编辑 / 视觉提示词工具
- 适合素材：封面图、信息图、技术图解、产品概念图、社媒配图、头像和主页资产、分镜板、UI 样机、视觉文档
- title：GPT Image 2 视觉生成工具
- format：模式感知的图像生成和编辑工作流
- channels：X、B 站、YouTube、视频号、小红书、官网素材、内部设计 brief
- Hook：先判断当前环境能不能直接出图，再把创意需求转成可复用、可归档、可交给图像模型执行的结构化 prompt。
- Structure：
  1. 先判断运行模式：本地 API 出图、宿主原生图像工具、或纯提示词顾问。
  2. 判断任务类型：文本生图还是基于原图编辑。
  3. 从模板类别中选择最贴近的视觉任务类型。
  4. 只读取对应模板，不一次性套用整个模板库。
  5. 把用户输入映射到主体、场景、构图、文本、风格、约束和输出尺寸等字段。
  6. 关键信息不足时，只问会显著影响画面的字段。
  7. 渲染最终 prompt，并按项目命名规则归档。
  8. 根据运行模式生成图片、委托宿主工具，或把 prompt 交给人工创作者使用。
- Length：单张图建议 1 个主视觉目标；复杂素材建议拆成 3-6 张系列图或分镜板。
- notes：
  - 适合账号：`thinking-lab` 适合技术图解、信息图和互动题视觉；`visiontree` 适合官方概念海报和视觉文档；`thinking-tree` 适合树形隐喻和概念场景；`nora` 适合试用日记截图感视觉；`milo` 适合工程流程图；`eli` 适合概念卡和慢解释图。
  - 适用素材：必须先明确图片用途，避免为了“好看”生成与口径无关的图。
  - 兼容字段：可映射到 `title`、`format`、`channels`、`structure`、`hook`、`length`、`notes`、`resources`。
  - 使用方式：在创作者 brief 中引用本工具时，应附上图片用途、目标账号、核心信息、可出现和不可出现的文字、是否允许虚构视觉元素。
  - 同步边界：这是准备区的工具型模板，不代表 `content-system` 已具备图像生成能力。
- resources：
  - 来源资料：【GPT-Image2 完全指南：一期讲透主流玩法（附我的生图 Skill）】<https://www.bilibili.com/video/BV1vi9UBhEKq/?share_source=copy_web&vd_source=c3f2a17dce62359215ab1773410de02b>
  - <https://github.com/ConardLi/garden-skills/tree/main/skills/gpt-image-2>
  - `skills/gpt-image-2/SKILL.md`
  - `skills/gpt-image-2/references/prompt-writing.md`
  - `skills/gpt-image-2/references/ui-mockups/`
  - `skills/gpt-image-2/references/product-visuals/`
  - `skills/gpt-image-2/references/infographics/`
  - `skills/gpt-image-2/references/technical-diagrams/`
  - `skills/gpt-image-2/references/avatars-and-profile/`
- 语气：具体、可执行、像给视觉设计师的制作 brief；少抽象形容词，多构图、对象、层级和约束。
- 禁忌：
  - 不生成或暗示未经验证的客户、指标、融资、结果数据。
  - 不把 VisionTree 表达成第二大脑、prompt 市场、模型库或替人思考的 AI。
  - 不在画面里写无法保证准确的小字、复杂表格或假界面数据。
  - 不把图像模型生成结果当成真实产品截图或真实用户证据。
  - 不跳过模式判断，避免没有图像能力时假装已经出图。
- 创作者提示：
  - 每次先写清楚“这张图服务哪条内容”，再选模板。
  - 用于 X 或短视频封面时，画面主张应少字、强层级；用于文章配图时可以提高信息密度。
  - 需要真实产品状态时，应使用真实截图或明确标注为概念视觉。
  - 复杂视觉任务优先拆成系列：封面、解释图、流程图、分镜，不要一张图承载所有信息。
- 人工判断点：
  - 是否允许生成概念化产品界面，还是必须等待真实界面。
  - 是否需要品牌统一视觉规则后再出图。
  - 哪些文字必须人工复核，哪些只作为视觉占位。
  - 生成图是否可对外发布，还是仅作为创作者参考。
- 同步到模板库：已同步
- 最近更新原因：2026-05-11 已作为介绍卡片同步到 `content-system` 模板库；保留完整工具说明在准备区，后续补真实案例截图。
