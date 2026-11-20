# Install Aether

Aether is an open-source **AI agent for Android** that runs an LLM chat with real tools
(bash, file read/write/edit, grep, find, ls), MCP servers, subagents and a local Alpine runtime.

## 1. Get the APK

Download the latest signed APK from
[releases](https://github.com/jcufyr6d5djj-beep/aether/releases/latest) — file name `Aether-vX.Y.Z.apk`.

Android 8.0 or newer. If Play Protect warns about an app from outside the store,
choose "install anyway"; every build is signed with the same key, so updates install
on top of the previous version without losing chats.

## 2. Configure a model

Open Settings → Providers and add an OpenAI-compatible provider: base URL, API key and
model id. Any provider that speaks the OpenAI chat-completions API works. The model
selector lives in the top bar of the chat.

## 3. First task

Ask for something that needs a tool, for example: "list the files in my workspace and
explain what this project does". Aether shows each tool call with its arguments and
result, and asks for confirmation before anything destructive.

## 4. Local runtime

Settings → Runtime lets you switch between the bundled Alpine (proot) environment and
Termux. Everything the agent runs stays on the device.
