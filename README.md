# One Click Delete

A private Trello Power-Up that adds a card button for permanently deleting the open card with one click.

The Power-Up uses the Trello Power-Up client library and Trello REST API authentication. It has no backend, no build step, and no npm dependencies.

## Setup

1. Create the GitHub repository named `trello-one-click-delete-powerup`.
2. Enable GitHub Pages:
   - GitHub repo -> Settings -> Pages -> Deploy from branch -> `main` -> `/root`.
3. Copy the final GitHub Pages URL.
4. Go to https://trello.com/power-ups/admin.
5. Create a new Power-Up.
6. Name it `One Click Delete`.
7. Set the iframe Connector URL to:

   ```text
   https://<github-username>.github.io/trello-one-click-delete-powerup/index.html
   ```

8. Generate a Trello Power-Up API key from the API Key tab.
9. Replace `PASTE_TRELLO_POWERUP_API_KEY_HERE` in `index.html` and `authorize.html` with the generated key.
10. Push the update to GitHub.
11. In Trello, open the target board.
12. Go to Power-Ups.
13. Add or enable the private Power-Up from the workspace.
14. Open a card and authorise the Power-Up.
15. After authorisation, open any card and click `Delete card` to permanently delete it and return to the board.

## Files

- `index.html` is the iframe Connector URL and declares the `card-buttons` capability.
- `authorize.html` opens the Trello REST API authorisation flow with `read,write` scope and `never` expiration.
- `styles.css` contains the minimal shared styling.

## Notes

- There is intentionally no confirmation prompt.
- No personal Trello token is stored or hard-coded.
- After deletion succeeds, the open card closes automatically.
