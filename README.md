# Agree

**Agree** is a lightweight Minecraft plugin that shows players a chest-style GUI when they join your server.  
In the middle is a book with your custom rules or info, and on the sides are two buttons (default: **Agree** / **Deny**).  
If they accept, they can play. If they deny, they’re kicked with a customizable message.

---

## Features

- 📘 **Join GUI** – Automatically opens a chest GUI every time a player joins.
- 📖 **Rule Book** – Center item is a book showing your custom message from the config.
- ✅ **Agree / ❌ Deny Buttons**  
  - Button names are fully configurable (you don’t have to use “Agree” / “Deny”).  
  - Agree lets the player continue and can send them a custom chat message.  
  - Deny kicks the player with a configurable disconnect message.
- 🎨 **Fully configurable text**  
  - GUI title  
  - Book lore lines  
  - Button names  
  - Kick message  
  All support classic `&` color codes.

---

## How it works

1. Player joins the server.  
2. The **Agree GUI** opens automatically.  
3. Player reads your rules/info in the center book.  
4. Player clicks:
   - **Agree** → GUI closes, optional “thanks for agreeing” message is sent.
   - **Deny** → Player is kicked with your custom decline message.

The GUI shows **every time a player joins**, so they must accept each session.

---

## Configuration

The config file lets you customize everything the player sees.

Example:

```yaml
# Agree plugin configuration
# This GUI shows EVERY time a player joins.
# They must click AGREE to play, or DECLINE to be kicked.

gui:
  # Title of the GUI (supports & color codes).
  title: "&cServer Agreement"

  # The text shown in the middle item (book) as lore.
  # Each line is one lore line. & codes allowed.
  message-lines:
    - "&7This server is not very fast or good in performance."
    - "&7Please &cdo not build lag machines &7or heavy farms."
    - "&7Try to keep things simple and have a fun time!"
    - ""
    - "&eBy clicking &aAGREE &eyou accept these rules."

  # Text for the buttons:
  agree-button-name: "&a[ CLICK TO AGREE ]"
  decline-button-name: "&c[ DECLINE AND DISCONNECT ]"

messages:
  # Shown in chat to the player after they agree.
  agreed: "&aThanks for agreeing! Enjoy your time on the server."

  # Kick message when a player clicks DECLINE.
  # This is the screen they see when they get disconnected.
  decline-kick-message: |
    &cYou declined the server agreement.

    &7This server is not very fast or good in performance,
    &7and it cannot handle lag machines or very heavy farms.

    &7To keep the server stable for everyone, we ask players
    &7not to build laggy contraptions or intentionally try to
    &7crash or slow down the server.

    &cWe are really sorry for the inconvenience.
    &7If you are happy to respect these rules, please
    &7join again and click &aAGREE &7next time.

    &7Thank you for understanding, and we hope to see you soon!
