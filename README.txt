SuperYatzy v23 – trin 3

Baseline: tested v23-trin2c.

ONLY new feature:
- Every action actually applied by the host (roll, hold, score) is serialized
  to public.games.game_state.
- Saves are queued so rapid actions cannot overwrite each other out of order.
- updated_at is updated with each save.
- The game UI and existing online behavior are unchanged.
- If a DB save fails, the game continues locally and the online status shows
  "Online – spil ikke gemt"; the browser console contains the error.

This does NOT add recovery/resume yet.

Test:
1. Create a NEW online game.
2. Let player 2 join.
3. Perform one or more rolls and holds.
4. Choose a category.
5. Refresh the games table / open game_state.
6. Confirm dice, held, rolls, scores, active and player names reflect the
   latest game state.

Visible version: v23-trin3.
