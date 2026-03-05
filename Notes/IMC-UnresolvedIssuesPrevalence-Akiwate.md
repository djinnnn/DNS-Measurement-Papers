---
type: paper
tags: [DNS, lame-delegation, measurement, IMC-2020]
measurement_platform: [[DNS Infrastructure]]
measurement_tools: [[custom DNS resolver]], [[zone enumeration]]
data_source: 全球 DNS 递归查询，大规模主动测量
geo_distribution: [[Global]]
network_env: [[IPv4]], [[IPv6]]
---

# IMC-UnresolvedIssuesPrevalence-Akiwate

## 论文信息
- **标题**: Unresolved Issues: Prevalence, Persistence, and Perils of Lame Delegations
- **作者**: Akiwate 等
- **会议**: [[IMC]] 2020
- **主题**: DNS lame delegation（无效委托）的普遍性、持续性和危害

---

## Measurement Ontology 提取

### 1. 测量方法
- **类型**: [[主动测量]]
- **方式**: 通过自定义 DNS 解析器进行大规模主动查询，检测 lame delegation 现象

### 2. 测量平台
- **基础设施**: [[DNS Infrastructure]]
- 针对全球 DNS 授权服务器进行委托完整性检测

### 3. 工具链
- [[custom DNS resolver]] - 自建解析器用于批量查询
- [[zone enumeration]] - 区域枚举技术识别委托关系
- 检测 NS 记录指向的授权服务器是否响应

### 4. 数据源
- **样本量**: 大规模 DNS 区域扫描
- **获取方式**: 主动查询 TLD 及以下各层级的 NS 记录，验证委托链完整性
- **区分**: 主要针对 [[Authoritative]] 服务器的委托配置

### 5. 时空维度
- **地理分布**: [[Global]] 全球范围测量
- **网络环境**: [[IPv4]] / [[IPv6]] 双栈环境
- **时间跨度**: 跨时间段持续观测 lame delegation 的持久性

### 6. 锐评（方法论局限与横向对比）

**局限性**:
- 主动测量可能无法反映真实用户遇到的 lame delegation 频率
- 某些无响应的 NS 记录可能是配置了 views 或响应过滤
- 无法区分临时故障与长期配置错误

**横向对比**:
- 与早期 DNS 健康研究相比，lame delegation 问题仍显著存在
- 相比 [[DNSSEC]] 部署研究，lame delegation 是更基础的配置完整性问题
- 与 [[DoH]]/[[DoT]] 研究关注点不同，本研究聚焦传统 DNS 委托链可靠性

---

## 核心发现（待补充）
> 需要进一步阅读论文补充具体统计数据和分析结论

## 相关研究链接
- [[DNS Measurement]]
- [[DNS Infrastructure]]
- [[Lame Delegation]]
