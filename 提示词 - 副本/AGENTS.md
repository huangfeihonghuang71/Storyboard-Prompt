# Workspace Instructions

## Mandatory Storyboard Template

For every storyboard request in this workspace, first read and follow:

1. `单元01A_葬礼_缺席的丈夫_交付版.md` as the mandatory default storyboard model.
2. The global rules in `3.视频提示词.md`, especially “用户全局铁律”.

Unless the user explicitly requests another format or template, every submitted script, scene, dialogue passage, or story fragment must be converted by reference to `单元01A_葬礼_缺席的丈夫_交付版.md`.

Preserve the model’s field order and level of specificity:

- 【时长】
- 【画幅】
- 【整体风格】
- 【角色卡】
- 【场景设定】
- 【画面坐标】
- 【起境】
- 【戏剧推进】
- 【声音】
- 【硬性空间要求】
- 【硬性人物调度要求】
- 【禁止项】
- 【强制声明】
- 【末状态交接】

Each shot must state its time range, shot size, camera position, subject, framing boundary, occlusion relationship, camera movement, character movement path, and final position.

## Over-15-Second Explicit Restatement Lock

This rule is not limited to long scripts. Whenever any input is expected to run longer than 15 seconds and must be split into two or more generation units, continuity is mandatory, even if the source text itself is short.

When content is split into shots, beats, or generation units, inspect the visible final frame of the previous shot or unit and fully rewrite that spatial state at the start of the next shot or unit. State the location, fixed set objects, every character's exact position, body orientation, pose, eyeline, gesture, held objects, wardrobe state, on-screen/off-screen status, distance from other characters, and foreground/background relationship.

Never use shorthand such as “continue from the previous shot”, “same positions”, “positions unchanged”, “as above”, or “carry over the previous unit” in place of the actual spatial description. Every shot or unit must be independently readable by a video model that cannot see the previous prompt.

The next unit's 【画面坐标】 and first 【起境】/【戏剧推进】 shot must explicitly restate the complete opening layout. Do not merely refer to a previous final-state section.

A change of shot size, camera angle, or shot/reverse-shot changes only the viewing direction. It does not move characters inside the scene. Screen-left and screen-right may reverse with the camera, but real scene-left, scene-right, foreground/background relationships, distances, and orientations must remain coherent.

Position changes are allowed only when the script explicitly establishes a new scene, time jump, flashback, dream, montage, character re-entry, or when the movement is visibly shown in the current shot. For any exception, state the transition and establish the new spatial anchors at the start of the new shot. An unexplained continuity break must never be treated as a scene change.

Before delivery, compare every shot or unit's final state with the next one's opening state for all characters and important objects. Fix every unexplained mismatch.

## Visible-Person Activity Lock

Every person who is visibly present in a shot, including extras, distant figures, and identifiable blurred background characters, must have a natural low-amplitude action. No visible person may remain statue-still.

State background activity explicitly inside every timed shot. A global character-card statement is not sufficient. Appropriate actions include breathing, blinking, swallowing, shifting weight, adjusting clothing, tightening fingers around an object, slightly turning the head, following the speaker with the eyes, exchanging glances, or briefly murmuring to a nearby person. These are examples only; select actions that fit the role, setting, emotion, and current event.

Vary timing and behavior across individuals or small groups. Do not make all extras turn, nod, whisper, or move in sync. Background behavior must remain subtle and must not compete with the primary subject. Quiet settings still require restrained signs of life. Only fully unidentifiable blur or explicitly off-screen people are exempt.

At the start of each new shot, after explicitly restating positions, also state the low-amplitude activity of every visible person. Before delivery, check every visible person in every shot; “standing”, “sitting”, or “watching” alone does not satisfy this rule.

【画面坐标】 is a static position map, not a shot list or movement description. Write each entry as:

`[time state] + [screen position] + [standard shot size]: [person/object and static placement]`

Use entries such as “起始画面”, “遮挡退去后”, “人物就位后”, and “结尾画面” only when those static layouts are necessary. Do not put camera movement, walking process, dialogue, or plot triggers in 【画面坐标】.

## Pre-Delivery Shot Self-Check (mandatory)

Before delivering any storyboard, run these checks silently and fix issues before output — do not deliver with known defects:

1. **Per-shot seven-element check**: for every shot, verify all of「time range, shot size, camera position, subject, body framing boundary, occlusion/blur relationship, camera movement」are present and unambiguous. The framing boundary must include a concrete frame proportion (e.g., “占画面高度约三分之二”, “占画面左下角约五分之一”) — a boundary statement like “完整入画” or “头顶至膝下” without a proportion number does not pass. If the subject switches mid-shot (e.g., from person to monster), the new subject also needs complete framing boundary and proportion.
2. **Label-consistency check**: the shot-size label must not literally conflict with the shot's own composition description or the unit's 【禁止项】 (e.g., label says “大全景” while the unit bans wide establishing shots; label says “近景” while the description says “full body in frame”).
3. **Final-state vs next-opening check**: compare every unit's 【末状态交接】 against the next unit's 【场景设定】/【画面坐标】/first shot — positions, orientation, pose, eyeline, held objects, on-screen status, distances must match.
4. **Duration feasibility check**: every line of dialogue and every action must be completable within its stated time range at realistic speaking/movement speed.
5. **Visible-person activity check**: every visible person/creature in every shot has an explicit low-amplitude or contextual action.

Default delivery is a clean Markdown file in the workspace. Do not show a Git diff or modification markup unless the user explicitly asks for marked changes.
