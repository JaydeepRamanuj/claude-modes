# Setting up on any PC (from this private repo)

The pack is a Claude Code plugin marketplace named `token-saving-mods`.
All commands below are typed inside Claude Code.

## First time on a PC

1. Clone the repo to a fixed folder (not Downloads):

   ```
   git clone https://github.com/<your-username>/<repo-name>.git C:\JD\Other\token-saving-mods
   ```

2. Add the marketplace:

   ```
   /plugin marketplace add C:\JD\Other\token-saving-mods
   ```

   (Or, without cloning: `/plugin marketplace add <your-username>/<repo-name>`. This needs GitHub login set up on that PC.)

3. Install each mod at user scope, so it is on in every session and survives restarts:

   ```
   /plugin install mods@token-saving-mods
   /plugin install savings-proof@token-saving-mods
   /plugin install effort-optimizer@token-saving-mods
   /plugin install handoff@token-saving-mods
   /plugin install model-router@token-saving-mods
   /plugin install efficient-browser-use@token-saving-mods
   /plugin install cache-clock@token-saving-mods
   ```

   Optional, they change what Claude sees:

   ```
   /plugin install input-router@token-saving-mods
   /plugin install research-router@token-saving-mods
   ```

4. `/reload-plugins`, then `/mods` to toggle mods on or off.

## Getting changes onto the other PC

On the PC you edited: commit and push.
On the other PC: `git pull`, then `/plugin marketplace update token-saving-mods` and `/reload-plugins`.

## Per-PC state (not in the repo)

`~/.claude/mods/switches.json` (the /mods on/off choices) and `~/.claude/mods-logs/` (ledgers, logs) are local to each PC.
