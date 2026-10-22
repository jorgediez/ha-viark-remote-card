# Viark Remote Card has moved

**The card now ships with the
[Viark Satellite Receiver integration](https://github.com/jorgediez/ha-viark),
from version 1.4.0.** This repository is archived and gets no more updates.

<p align="center">
  <img src="https://raw.githubusercontent.com/jorgediez/ha-viark-remote-card/main/images/screenshot.png" alt="Viark Remote Card" width="320">
</p>

Home Assistant's community store (HACS) lists a card that only works with one
integration as part of that integration, so the card moved there, with its
history. Installing the integration installs the card, and the integration loads
it on every dashboard: there is no dashboard resource to add.

Its documentation is now in the integration's README:
[Remote card](https://github.com/jorgediez/ha-viark#remote-card). Report problems
in [the integration's issues](https://github.com/jorgediez/ha-viark/issues/new/choose).

## Switching over

Your cards keep working as they are: the card type (`custom:viark-remote-card`)
and every option are the same. Remove this copy, or the dashboard may keep
loading it instead of the new one:

1. Update the Viark integration to 1.4.0 or newer and restart Home Assistant.
2. **Installed through HACS:** open HACS, find **Viark Remote Card**, and choose
   **⋮ → Remove**. HACS deletes its dashboard resource too. Then remove
   `https://github.com/jorgediez/ha-viark-remote-card` from **HACS → ⋮ → Custom
   repositories**.
3. **Installed by hand:** delete the `/local/ha-viark-remote-card.js` entry under
   **Settings → Dashboards → ⋮ → Resources**, and the file from `config/www/`.
4. Reload the browser. In the companion app, use **Reset frontend cache**, under
   **Settings → Companion app**, in Debugging on iOS or Troubleshooting on
   Android.

The browser console shows `VIARK-REMOTE-CARD v1.4.0` (or newer) once the new card
is in use. More details are in
[Coming from the separate card](https://github.com/jorgediez/ha-viark#coming-from-the-separate-card).

The releases here stay available, but they will not be updated.

## License

[MIT](LICENSE)
