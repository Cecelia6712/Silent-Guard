# Silent-Guard · 沉默守卫

> "Every unauthorized access leaves an indelible trace beneath the timestamp."
>
> 「每一次未经授权的访问，都会在时间戳下留下不可磨灭的痕迹。我坚信凡事皆有迹可循。」

<p align="left">
  <img alt="Status" src="https://img.shields.io/badge/Status-Active%20Development-orange">
  <img alt="License" src="https://img.shields.io/badge/License-MIT-green">
  <img alt="Python" src="https://img.shields.io/badge/Python-3.8%2B-blue">
  <img alt="Purpose" src="https://img.shields.io/badge/Purpose-Defensive%20%7C%20Forensic-black">
</p>

---

## 1. 这是什么 / What This Is

**Silent-Guard 是一个纯本地运行的防御性 Python 工具集，用于对用户自有设备上的文件进行完整性监控与访问取证。**

**Silent-Guard is a purely local, defensive Python toolkit for file integrity monitoring and access forensics on devices you own.**

它**不**发起任何网络连接，**不**向外部传输数据，**不**包含攻击、提权、持久化或远程控制逻辑。它只做两件事：

- **完整性监控**：对指定目录生成 SHA-256 基线，检测篡改、替换、删除与新增。
- **蜜罐追踪**：布置无害诱饵文件，通过状态指纹变化记录访问事件的时间、主机名与本地 IP。

---

## 2. 允许与禁止的用途 / Permitted & Prohibited Uses

### ✅ 允许 / Permitted

- 对**你拥有合法所有权的**设备、目录或文件进行完整性校验与篡改检测。
- 在**你被明确授权管理**的机器上部署蜜罐与访问审计。
- 数字取证、事件响应的学习与研究，分析对象为**你合法持有的数据或介质**。
- 在受控测试环境中验证文件监控逻辑。

### ❌ 严格禁止 / Prohibited

- 在**他人所有的设备**上，或在**未经授权的网络与目录**中部署或运行本工具。
- 以监控、追踪、骚扰、人肉、敲诈或侵犯他人隐私为目的使用本工具。
- 将本工具的任何输出用于非法侵入、数据窃取或未经授权的取证。
- 将本工具改造或包装为具有隐蔽监控、远程控制或数据外传功能的产品。
- 任何违反《中华人民共和国网络安全法》《个人信息保护法》《数据安全法》及使用者所在司法辖区法律的行为。

---

## 3. 法律依据与使用者责任 / Legal Basis & User Responsibility

使用者必须自行确保其对部署本工具的设备与目录拥有**合法所有权或明确授权**，并对使用行为承担全部法律责任。

在非本人所有的设备或环境中使用本工具，可能构成对《中华人民共和国网络安全法》第二十七条（禁止非法侵入他人网络、干扰网络正常功能、窃取网络数据）、《个人信息保护法》及《数据安全法》相关条款的违反。

本工具的开发者与贡献者**不对任何使用者违反上述法律的行为承担责任**。使用者应在具体场景中自行寻求独立的法律意见。

---

## 4. ⚠️ 免责声明 / Disclaimer

本软件按 **“AS IS”** 提供，不附带任何明示或默示的担保，包括但不限于适销性、特定用途适用性和不侵权的担保。在任何情况下，作者或版权持有人均不对因本软件或本软件的使用而产生的任何索赔、损害或其他责任承担责任，无论是合同之诉、侵权之诉还是其他形式的诉讼。

本 README 中的合规说明**不构成法律意见**。

完整许可条款见仓库根目录 [`LICENSE`](./LICENSE)。

---

## 5. 技术上的诚实说明 / Honest Technical Note

本工具对**纯读取**行为的捕获依赖文件系统的 `atime` 更新策略。在 `relatime` 或 `noatime` 挂载下，纯读取可能不被可靠捕获。这是操作系统层面的限制，不是本工具的缺陷。对**篡改、替换、删除、移动**的检测不受此影响。

---

## 6. 报告滥用 / Reporting Misuse

维护者保留在项目文档中公开声明与任何滥用行为无关的权利。

---

## 7. License

MIT © Silent-Guard Contributors. See [`LICENSE`](./LICENSE).
