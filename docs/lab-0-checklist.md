# Lab 0 completion checklist

Keep this file factual: checked means verified, not merely planned. Repository settings require the repository owner or an administrator; ordinary write access cannot configure them.

## Shared deliverables

- [x] Record the four members and two services per person.
- [x] Define all eight service boundaries and data owners in the public README.
- [x] Add a Mermaid architecture diagram and full interaction table.
- [x] Record the confirmed Go + TypeScript/NestJS split and technology trade-offs.
- [x] Define REST request/response schemas, WebSocket frames and asynchronous events.
- [x] Define contribution, review, testing and versioning policies.
- [x] Add a PR template and automated PR-policy workflow.
- [ ] Team review of proposed gameplay constants and contracts.
- [x] Establish remote `main` and `dev` branches.
- [x] Publish Sava's Battle and Tamagotchi contract READMEs and prepare their real submodule pointers.
- [x] Create repository issues for remaining Lab 0 actions and future implementation planning.
- [ ] Enable required approvals/checks on `main` and `dev`.
- [ ] Create and link a real GitHub Project; seed tasks and set owners/statuses.
- [ ] Add all eight actual submodules pointing to pushed commits.
- [ ] Verify all eight private READMEs contain their relevant contracts.

## Owner setup: branch protection

Tracked in [issue #2](https://github.com/MadalinaDev/tamagotchi-go-team-12/issues/2). Verified 2026-09-10: ruleset `protect-main-dev` (ID 22823249) is active for `refs/heads/main` and `refs/heads/dev`, blocking deletion and non-fast-forward updates and requiring one approving review. It does not yet require dismissal of stale approvals, resolved conversations, or the `PR policy` status check. Current contributor permission is WRITE, not ADMIN, so adjustments remain an owner action.

Mădălina (or another administrator): Repository **Settings → Rules → Rulesets**, or **Branches → Add branch protection rule**.

For both `main` and `dev`:

1. Require a pull request and **one approval**.
2. Dismiss stale approvals when new commits are pushed.
3. Require resolved review conversations.
4. Require the **PR policy** status check (run the first PR once so the check is selectable).
5. Block force pushes and branch deletion. Avoid bypass permissions.
6. Leave linear-history enforcement off on `main`; release merges use merge commits.

Under **Settings → General → Pull Requests**, allow squash merging and merge commits. Use squash for task → dev and merge commits for dev → main. The workflow validates branch targets; GitHub's global merge-method switches do not enforce a different method per branch. Reviewers must choose the correct method.

Private repositories intentionally do not invite teammates. Do not copy the common repo's teammate-approval requirement to private repos where reviewers cannot access the content.

## Project board

Tracked in [issue #3](https://github.com/MadalinaDev/tamagotchi-go-team-12/issues/3). The user chose Mădălina to create/link the board because the current GitHub token lacks Project scopes. The [12 prepared issues](https://github.com/MadalinaDev/tamagotchi-go-team-12/issues) can be added directly to it.

An administrator or authorized Project owner can create **Tamagotchi Go — PAD Team 12** with statuses **Todo**, **In Progress**, **In Review**, **Done**. Link it through the repository's **Projects** tab. A Project may belong to a user or organization; it is not an ordinary Git repository file.

Seed the board from [backlog.md](backlog.md), preferably using repository issues. Add team members with write access to the Project, assign tasks using their actual GitHub usernames and put the Project URL in the main README. Do not substitute a Markdown task list for the linked board.

## Each service owner

1. Create two private repositories; add `.gitignore` and an initial README.
2. Invite professor(s), using contacts from the course. Do not invite teammates.
3. Copy the common conventions, owned schemas/APIs/events and relevant dependency contracts from the reviewed shared README into each private README. Include game rules and recovery behavior that the service owns. A link alone is insufficient for grade 10.
4. Push the initial commit from your account.
5. Submit repository URLs and submodule pointers to the common repo through a PR.
6. Confirm Excel links and help review shared contracts affecting your services.

## External course actions

- [ ] Team Definition Excel completed with the final membership (Sabina replaced Cristi).
- [ ] All required repository links entered in the course Excel.
- [ ] Professor invitations sent and access confirmed.
- [ ] Presentation slot reserved in the Teams sheet before 08:00 on presentation day.
- [ ] Team can explain its design and contribution from the presentation laptop.

The PDF allocates one week and does not contain the Excel URL or professor GitHub usernames. These actions must be confirmed by the team; no automated GitHub setup can verify them.
