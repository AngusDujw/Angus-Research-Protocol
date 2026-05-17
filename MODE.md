# Research Mode State

- `mode`: `unset`
- `updated_at`: `YYYY-MM-DD HH:MM`
- `set_by`: `bootstrap.md`

---

## 状态判定（与 AGENTS.md § 2.2 一致）

| `bootstrap.md` | `MODE.md::mode` | 行为 |
|---|---|---|
| 存在 | 任意 | **未初始化**，必须走 bootstrap 向导 |
| 不存在 | `newbie` / `expert` | 按该模式正常工作 |
| 不存在 | `unset` 或文件缺失 | 协议异常，提示用户从模板重建 `bootstrap.md` |

---

## 模式说明

### newbie
- 一步一引导，默认给最小下一步。
- 每步同步更新文档，帮助建立流程感。

### expert
- 结论先行，减少教学式解释。
- 支持批量推进，优先效率与实验吞吐。

---

## 切换规则

- 首次由 `bootstrap.md` 写入。
- 后续若用户明确说"切换为新手/老手模式"，立即更新本文件三字段（`mode / updated_at / set_by=user`）并生效。
- Agent **不得**自行切换模式，必须由用户发起。
