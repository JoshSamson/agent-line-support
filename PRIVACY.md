# Agent Line privacy policy

*Effective 20 November 2026. Published at https://github.com/JoshSamson/agent-line-support/blob/main/PRIVACY.md and inside the app under Settings, Privacy.*

Agent Line is an iPhone app for calling voice agents that run on a server you choose, and for receiving calls from them. It is published by Joshua Todes.

## In short

- Calling your agents contacts only the servers you add. Nothing goes to the publisher.
- Incoming calls are optional and off until you switch them on. Switching them on registers your phone with a ring service the publisher runs, so that an agent can ring it.
- Switching them off deletes that registration.
- The app has no account, no analytics, no advertising and no tracking.

## What stays on your phone

- The servers you add: each one's name, address and secret, kept in the iPhone Keychain.
- Your call history: which agent, when, for how long, and whether you missed the call.
- The photo or icon you choose for an agent.
- Your theme choice.
- If Incoming calls is on: the Phone ID and the secret the ring service gave this phone, kept in the iPhone Keychain.

Removing a server removes its agents' photos and its calls. Deleting the app removes the rest, except Keychain items, which iOS may keep.

## What goes to the servers you add

When you add a server, the app asks it for its list of agents. When you call an agent, your voice goes to the call service that server names, so the agent can hear and answer you. Whoever runs that server decides what happens to the audio and to anything you say. The publisher does not run those servers and cannot see or hear your calls.

This is unchanged from version 1.0, and it contacts nothing of the publisher's.

## Incoming calls

Incoming calls let an agent on a server you have added ring your iPhone. They are off until you switch them on in Settings. Each server also has its own "This server may call me" switch.

Apple only lets an app's publisher send a ring to that app, so every ring passes through a ring service the publisher runs. Rings are delivered through Apple's push notification service.

### What the ring service stores

When you switch Incoming calls on, the app registers your phone with the ring service. For each registered phone it stores:

- the push token Apple gives the app for incoming calls on this phone;
- a Phone ID, which is a random identifier the ring service creates. The app shows it in Settings, About, so you can quote it when asking for support;
- a scrambled form (a hash) of the secret the app uses to prove it is this phone;
- one ring address for each server you allow to call you, with a hash of that address's secret. The ring service does not know the server's name or address, or which server an address was given to;
- how many times the phone has been rung today, the date it was last rung, and the daily limit that applies to it;
- a short label, only if the publisher adds one when handling a support request.

### What passes through and is not kept

- Each ring carries an identifier for the ring, and the agent's identifier and name, so your phone can show who is calling. The ring service passes these to Apple's push service and does not keep them.
- The ring service sees the internet address of whatever contacts it. It uses these addresses only to limit abuse, and keeps them for seven days at most.

### What the ring service never has

- Anything said in a call. Calls do not pass through it.
- The address or key of any call.
- Your name, email address or any account. The app has none.
- Which server belongs to whom.

### Deleting it

- Switching off "This server may call me" for a server deletes that server's ring address at once.
- Switching Incoming calls off deletes the phone's registration: its push token, its Phone ID, its ring addresses and its counts.
- If you delete the app without switching Incoming calls off, the registration is deleted after 90 days without a ring.

### What your server receives

When you allow a server to call you, the app gives that server a ring address and its secret, and the name of your phone. The server uses the address to ring you. It never receives your push token. Switching the server's switch off makes that address stop working.

## Permissions

- Microphone: to speak on a call. Asked the first time you call.
- Camera: to scan a server's pairing code. The image is read on the phone and not kept.
- Photos: you pick a photo for an agent with the system picker. The app sees only the photo you pick.
- Local network: to reach a server on your own network.

## What the publisher does not do

The publisher does not sell or share any of this, does not use it for advertising, and does not combine it with information from anywhere else.

## Children

Agent Line is not directed at children.

## Contact

Questions about this policy, and requests about a Phone ID, can be raised at https://github.com/JoshSamson/agent-line-support/issues. Never paste a pairing link or a server secret into an issue.

## Changes

If this policy changes, the new version will be published at the same address with a new effective date.
