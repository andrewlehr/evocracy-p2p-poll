# 🗳️ Simple P2P Poll & Chat

This is a minimal prototype of a decentralized governance tool built for the **Demcode Evocracy** experiment. It allows for basic deliberation and voting without a central database or server-side logic.

## What it does
- **P2P Connectivity:** Uses WebRTC (via PeerJS) to link browsers directly.
- **Mesh-capable:** Allows multiple connections to sync the same poll state.
- **Live Sync:** Changes to the poll topic, options, or votes are broadcast to all connected peers.
- **Chat:** A simple sidebar to discuss the poll in real-time.

## How to use it
1. Open the page: [https://andrewlehr.github.io/evocracy-p2p-poll/]
2. Set your **Nickname** and click "Set".
3. Share your nickname with a friend.
4. One person enters the other's nickname in the **Connect** box and clicks "Add Peer".
5. Once connected, you can set a topic, add options, and vote.

## Technical Notes
- **Data Persistence:** There is no database. If everyone closes their browser, the data is lost.
- **Networking:** It uses a public signaling server to find peers, but the actual data (votes/chat) stays between the browsers.
- **Conflict Handling:** Uses a simple "Last Write Wins" broadcast to keep peers in sync.

## Transparency
This code was generated with the assistance of **Gemini (Google AI)** to quickly prototype the WebRTC networking logic. The goal was to create a clean, readable foundation that is easy for others to merge or modify during the next phase of the experiment.