SuperYatzy v24.5 – recovery terning-sync fix

Baseline: tested v23-trin3-ui4.

UI6 adds recovery of an active online game after the browser/app is closed.
The local session marker is used to offer recovery, and the complete game
state is loaded from public.games.game_state before reconnecting to Realtime.
The recovery dialog uses Ja / Nej.

Visible version: v24.5.

Statistik trin 1: Et afsluttet online-spil gemmes én gang i public.game_history
med deltagere, fulde scores og vinder, så enkel indbyrdes statistik senere
kan bygges ovenpå. Kræver INSERT-policy på game_history.
