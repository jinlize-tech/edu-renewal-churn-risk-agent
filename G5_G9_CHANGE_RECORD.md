# G5/G9 产品修改记录

- 产品编号：$(@{number=27; product_id=JLZ-EDU-AG-006; chinese_name=续费流失风险预警; english_name=Renewal Churn Risk Agent; repository_name=edu-renewal-churn-risk-agent; repository_url=https://github.com/jinlize-tech/edu-renewal-churn-risk-agent; product_type=Agent; category_code=02; category=02 销售转化中心; description=续费风险识别和客户流失预警分析。; target_users=System.Object[]; core_input=续费周期、消课进度、家长互动、满意度、投诉、付款和历史续费; main_output=风险分层、预警原因、干预优先级、沟通计划、升级条件和数据缺口; product_risk=将风险评分误当确定性预测或打扰家长; dedup_label=需要明确差异化; dedup_note=与MT-CRM区分：提供分析和干预建议，不承担客户数据存储、自动化营销或CRM流程。; development_status=Planned / 待研发; license=Apache-2.0; spec_version=1.0.0; workbuddy_status=PLANNED_FOR_WORKBUDDY}.product_id)
- 产品名称：续费流失风险预警
- 基线：EDUCATION_BASELINE_V1.0.0
- 基线提交：$BaselineCommit
- 原版本：1.0.0
- 新版本：1.0.1

## 本次修改

1. 强化产品专属执行流程、输入核对和输出验收规则。
2. 新增 scripts/validate_input.js，实际检查必填字段、冲突、未确认数据和敏感信息。
3. 新增正常、缺失、冲突、敏感信息和非法JSON场景输入。
4. 测试升级为 T1–T7 分层并保存逐项检查结果。
5. 安装包加入 Apache-2.0 LICENSE 和 THIRD_PARTY_NOTICES.md。
6. 安装包升级为 1.0.1，加入许可证、第三方声明和输入校验脚本，保留 1.0.0 ZIP。
7. 按本产品冻结规格补充专属处理规则、输入到成果的核对矩阵和去重边界。

## 产品专属增强

- 核心任务：续费风险识别和客户流失预警分析。
- 主要风险：将风险评分误当确定性预测或打扰家长
- 去重边界：与MT-CRM区分：提供分析和干预建议，不承担客户数据存储、自动化营销或CRM流程。

- 按线索阶段、客户需求、决策角色、时间窗口和最近一次有效沟通建立判断依据。
- 区分客户原话、顾问记录和推断，不能把未确认意向当作成交承诺。
- 将下一步动作写到责任人、时间、渠道和完成标准，避免只给沟通话术。
- 涉及敏感客户信息时仅保留完成当前判断所需字段，不扩大到无关画像。

## 运行边界

- 本地模型行为：NOT_RUNTIME_VERIFIED
- WorkBuddy平台验证：WORKBUDDY_VALIDATION_NOT_IN_SCOPE
- 本轮不执行上传、安装、审核或正式发布。
