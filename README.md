Agree is a lightweight Minecraft server plugin that ensures players read and accept your rules before they can play.

When a player joins, a clean chest-style GUI opens automatically. A book in the center displays your custom message (rules, info, terms, warnings — whatever you need). On the sides are two buttons: accept and deny. Both button names are fully configurable, so you’re not locked into “Agree” and “Deny”.

If a player accepts, the GUI closes, they’re allowed to play, and they can receive a custom chat message. If they deny, they are immediately kicked with a configurable disconnect message. All text supports classic `&` color codes, including the GUI title, book message lines, button names, the agree message, and the kick message.

Agree is ideal for simple rule popups, performance warnings, or any “you must accept this before playing” agreement that should appear every time a player joins.

---

## Version highlights (more shown on changelog)

- **v1.0.3**
  - Added a short **agree delay** so players can’t instantly click Agree.
  - Added a configurable **agree sound** for better feedback.
  - Added a cleaner **startup console message** with the plugin version and Modrinth link.
  - Added an **update check** on startup.

- **v1.0.2**
  - Fixed duplicate acceptance log spam: the plugin now logs each player’s username and UUID **only once** when they click **Agree**, keeping `accepted.log` clean.

- **v1.0.1**
  - Added acceptance logging: when a player clicks **Agree**, their username and UUID are saved to a log file in the plugin’s **Agree** folder.

- **v1.0.0**
  - Initial release.
