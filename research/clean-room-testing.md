# Testing outside the development context

The fragment is deliberately taught. Here, clean-room means no extra private Mesh context, inherited conversation or evaluator answers. It does not mean an untrained model or proof of universal isolation.

## Recommended first route: the second computer

Use a separate OS/tool profile on the second PC or laptop. Do not import the development machine's agent configuration, hooks, plugins, skills, private corpus, language profiles or conversation history. Record any administrator/provider defaults that remain.

For the first manual trial, use a text conversation without repository/file tools. Paste only the four sender inputs listed in the [example](../examples/public-fragment/README.md). Use a second new conversation for the recipient with only its three allowed inputs. Inspect evaluation files only after freezing both answers. Keep model and settings fixed for a comparison; give every condition the same public primer. A new device with synced custom instructions or a resumed conversation is not automatically a clean condition.

Only the public text package is needed. No model-weight transfer, WSL, Geotopie, LSP or build is required. The public text is reusable under the terms in [LICENSE.md](../LICENSE.md); no private language profile is required. Hosting and contact availability are separate from those reuse permissions.

## What Codex sandboxing does and does not establish

Codex sandbox settings govern model-generated command execution and filesystem/network permissions. Codex also discovers user and project instructions. Therefore a read-only sandbox alone does not establish absence of private priming, hooks or inherited configuration. Separate runtime permissions from the model's input context. [Security documentation](https://developers.openai.com/codex/security/) and [instruction discovery](https://developers.openai.com/codex/guides/agents-md/).

For a reduced local CLI condition, use a new Codex home, a separate participant directory outside the development vault and a new invocation for each participant. Do not clone the private corpus or expose the evaluator directory. Existing machine/organisation policies may still apply; record them rather than trying to bypass them.

## Optional PowerShell 7 CLI template

The following is a manual setup template, not an executed trial. It assumes a clean machine/profile, an installed Codex CLI and a separately chosen model actually available to that account. Never copy credentials into this repository.

```powershell
$studyRoot = Join-Path $env:TEMP ('mesh-public-' + [guid]::NewGuid())
$studyHome = Join-Path $studyRoot 'codex-home'
$participantDir = Join-Path $studyRoot 'participant'
New-Item -ItemType Directory -Path $studyHome,$participantDir | Out-Null
$env:CODEX_HOME = $studyHome
codex login
codex --version
codex exec --help
```

Review the new home and participant directory for extra instructions/hooks/configuration. Also inspect instruction files in the relevant parent/project chain. Sign in normally; do not copy the original Codex home or dump authentication values. Choose the supported model ID in the next command; no particular model is assumed available.

From the public clone, assemble only the sender inputs:

```powershell
$poc = Join-Path (Get-Location) 'examples/public-fragment'
$prompt = (@('primer.txt','carrier.txt','case-01.txt','sender.txt') | ForEach-Object {
    Get-Content -Raw -LiteralPath (Join-Path $poc $_)
}) -join "`n`n"
$answerPath = Join-Path $studyRoot 'sender-answer.txt'
$eventPath = Join-Path $studyRoot 'sender-events.jsonl'
$prompt | codex exec --ignore-user-config --ephemeral --sandbox read-only --skip-git-repo-check -C $participantDir -m '<available-model-id>' -o $answerPath --json - | Tee-Object -FilePath $eventPath
```

For the recipient, build a new prompt from `primer.txt`, `receiver.txt` and the frozen sender answer, then run a **new** `codex exec` with separate output names. Do not use `resume` or `fork`. Repeat in fresh conversations for case-02 and carrier controls. Preserve the explicit event and answer outputs; do not rely on ephemeral rollout storage.

This template does not claim a hard read-isolation boundary: read-only execution may still read other allowed files. The prompts prohibit tools, and a trial with extra tool reads or injected private instructions must be marked contaminated. For technically enforced input isolation, use a separately configured VM/container or a tool-free inference client, then record the actual policy and exposed inputs. An empty working directory alone is insufficient.

`CODEX_HOME` selects local state/configuration, `--ignore-user-config` skips its base config, and `--ephemeral` suppresses saved rollout files. None alone proves a context-free run. The flags above were checked against local CLI help 0.164.0 when preparing this draft; recheck your installed version. [Configuration locations](https://developers.openai.com/codex/config-advanced/) and [CLI reference](https://developers.openai.com/codex/cli/reference/).

## Record before drawing a conclusion

Keep model/client versions, active instruction sources, allowed inputs, raw outputs, retries and independent scoring. A model's assertion that it saw no hidden context is not a substitute for inspecting setup and delivery records. Run the public demo first; plan a larger experiment only after the basic procedure is understood.
