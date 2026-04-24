# n8n Telegram to Calendar Assistant

A lightweight n8n workflow that processes Telegram messages (text or voice), transcribes audio, uses AI to decide calendar actions, and interacts with Google Calendar (Create/Get/Update/Delete). Replies back via Telegram and can send optional Gmail notifications.

---

## What it does

- Handles Text or Voice inputs from Telegram.
- Transcribes voice messages.
- Uses AI to interpret intent and perform Google Calendar actions (create, get, update, delete).
- Replies to the user via Telegram; optional Gmail output.

---

## Core Nodes

- Telegram Trigger
- Get a file
- Transcribe a recording
- AI Agent (OpenAI LangChain)
- Google Calendar Tool (Create/Get/Update/Delete)
- Simple Memory
- Edit Fields / Switch (Text or Audio)
- Send Telegram message
- Optional: Gmail

---

## How data flows

Telegram Trigger → determine Text or Voice → (Voice → Transcription) → AI agent decides calendar action → Google Calendar tools execute → Telegram reply (or Gmail if needed).

---

## Example use cases

- User sends a voice message: “Schedule a meeting tomorrow” → transcript → create event → confirmation sent back.
- User sends text: “Update next week 10–11” → AI decides update → calendar updated → confirmation sent.
- User sends a non-calendar request: AI routes to a generic reply via Telegram.

---

## Quick Start

- Import the workflow JSON into your n8n instance.
- Configure credentials: Telegram, Google Calendar, and OpenAI/LangChain as needed.
- Run and test with a Telegram message or voice note.

---

## Requirements

- n8n with support for LangChain/OpenAI nodes
- Telegram Bot credentials
- Google Calendar OAuth credentials
- Optional Gmail credentials