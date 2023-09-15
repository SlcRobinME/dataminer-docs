---
uid: Connector_help_Imagine_Communications_Selenio_AAEX
---

# Imagine Communications Selenio AAEX

The **Imagine Communications Selenio AAEX** is a type of card that can be slotted into a Selenio Chassis. Unlike other Imagine Communications Selenio cards, this card does not contain any additional parameters beyond the general status information. The AAEX is an extension card that should be slotted next to another card. This will unlock new content and options for the adjacent card.

## About

The **Versioning** for the connector is specifically engineered to tie in with the firmware version of the card the connector supports. It uses the following format: X.X.X.Y, with X.X.X being the firmware version of the card, and .Y the specific driver iteration for this firmware. E.g.: *5.0.28.2* means the connector is the second iteration for firmware *5.0.28.*

The current version is *1.2.0.2.*

## Installation and configuration

### Creation

This connector uses a Simple Network Management Protocol (**SNMP**) connection and requires the following input during element creation:

**SNMP CONNECTION:**

- **IP address/host**: The polling IP of the device.
- **Device address**: Slot number that the card is plugged in at. Range *1-14.*

**SNMP Settings**:

- **Port number**: The port of the connected device, by default *161*.
- **Get community string**: The community string needed to read from the device. The default value is *public*.
- **Set community string**: The community string needed to set to the device. The default value is *public.*

### Timing

All data gets retrieved from the device using timers:

- Slow Timer that triggers every hour and retrieves slow-changing parameters such as the device version.
- Medium Timer that triggers every 2 minutes and retrieves status parameters such as the temperature, slot state and protection.

## Usage

The **Driver** contains only a single page:

- ### General:

  Contains general data such as the card version, slot temperature, state and protection.