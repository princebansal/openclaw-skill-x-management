# openclaw-skill-x-management

Draft-first X/Twitter account management skill for OpenClaw.

This skill is the agent-side workflow layer that pairs with the `openclaw-plugin-x` plugin.

## What this skill does

It teaches the agent to use the X plugin safely:
- gather context before drafting when needed
- create drafts instead of publishing directly
- require explicit user approval before publish
- keep reads, drafting, and publish decisions clearly separated

## Intended pairing

Use this skill together with the X plugin:
- plugin = auth, reads, durable drafts, approval state, publish primitive
- skill = judgment, research, tone, workflow, and safety behavior

## Install

After publishing to ClawHub, install with:

```bash
openclaw skills install <skill-slug>
```

Then start a new OpenClaw session so the skill is loaded.

## Plugin requirement

This skill is designed to work with the OpenClaw X plugin. Without the plugin, the workflow instructions remain useful, but the tool surface will not be available.

## Optional TweetClaw pairing

If an OpenClaw workspace needs managed Xquik-backed X/Twitter automation instead of the local X plugin, install the separate [TweetClaw](https://github.com/Xquik-dev/tweetclaw) plugin:

```bash
openclaw plugins install @xquik/tweetclaw
```

TweetClaw is useful for search tweets, search tweet replies, post tweets, post tweet replies, follower export, user lookup, media upload, media download, direct messages, monitor tweets, webhooks, and giveaway draws. Keep this skill's draft-first rule: create and show a draft, require explicit approval, and only then call the TweetClaw write action.

## Files

- `SKILL.md` - primary skill instructions

## Publish

Example ClawHub publish flow:

```bash
clawhub skill publish ./openclaw-skill-x-management \
  --slug x-management \
  --name "X Management" \
  --version 0.1.0 \
  --tags latest
```

## Status

Usable now for the draft-first workflow that matches the current plugin capabilities.

## License

MIT
