# Escape Director Device SDK

Bring your own Arduino prop code into Escape Director. Keep your puzzle logic;
the SDK connects its state, commands and completion signals to the Room.

Adapters for the Arduino UNO R4 WiFi and GIGA R1 WiFi are included. Other
Arduino boards with USB, Wi-Fi and enough memory can use the SDK through a
small [board adapter](https://docs.escapedirector.com/developers/add-a-board-adapter), and other platforms can speak
its [MQTT protocol](protocol.md) directly. The SDK is free to use and change
under the [MIT License](#license).

Not writing firmware? A prop that already sends MQTT or HTTP messages doesn't
need the SDK: connect it as an
[existing device](https://docs.escapedirector.com/build-your-rooms/connect-existing-devices).

## Documentation

The guides live in the [Developers section of the Escape Director docs](https://docs.escapedirector.com/developers/overview):

| Task | Guide |
| --- | --- |
| Upload the example and connect it to a Room | [Connect your first Arduino prop](https://docs.escapedirector.com/developers/quickstart) |
| Connect a sketch you already have | [Add the SDK to your sketch](https://docs.escapedirector.com/developers/add-the-sdk-to-your-sketch) |
| Work with a coding agent | [Build props with a coding agent](https://docs.escapedirector.com/developers/build-with-a-coding-agent) |
| Every call, its limits and outage behavior | [ed::Room reference](https://docs.escapedirector.com/developers/room-api-reference) and [EscapeDirectorRoom.h](src/EscapeDirectorRoom.h) |
| Copy a working sketch | [Example sketches](https://docs.escapedirector.com/developers/example-sketches) |
| Check boards, versions and limits | [Supported boards and limits](https://docs.escapedirector.com/developers/supported-boards) |
| Add a different board | [Add a board adapter](https://docs.escapedirector.com/developers/add-a-board-adapter) and [BoardAdapter.h](src/BoardAdapter.h) |
| Fix a problem | [Troubleshoot SDK firmware](https://docs.escapedirector.com/developers/troubleshoot-your-firmware) |
| Wire protocol (SDK maintainers) | [Protocol](protocol.md) |
| Contribute or build a download | [Contributing](CONTRIBUTING.md) |
| Report a security problem | [Security policy](SECURITY.md) |

Working with an AI coding agent? Open this folder in it. The root
[AGENTS.md](AGENTS.md) is the agent's entry point, and `CLAUDE.md` points to it
too.

## What you need

- A board with an adapter: UNO R4 WiFi or GIGA R1 WiFi.
- Arduino IDE or Arduino CLI, ArduinoJson 7 and ArduinoMqttClient 0.1.8.
- Escape Director and Room Connector for pairing and running the integration.

To change the SDK itself, install Node.js 24.18+, a C++17 compiler and
ArduinoJson, then run `npm ci` and `npm run check`. The Node tools are for
development only; your controller does not run Node.

The SDK is for show control. It is not a safety controller; keep emergency exits,
safety interlocks and other life-safety functions independent. Test on a spare
board with prop loads disconnected before adapting an installed controller.

## License

SDK code, examples, documentation and local tooling are licensed under the
[MIT License](LICENSE): use, modify and redistribute them however you like,
including in commercial props, as long as the license notice stays with the
source. [Escape Director trademarks](TRADEMARKS.md) remain reserved.
Separately installed libraries and board cores retain their own licenses; see
[third-party dependencies](THIRD_PARTY.md).
