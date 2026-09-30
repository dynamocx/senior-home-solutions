# Senior Home Solutions: Website Work

Shared workspace for adding and improving pages on seniorhomesolutions.com (production) with Claude Code and the Elementor MCP.

- `CLAUDE.md` holds the project knowledge Claude loads automatically. It imports the shared playbook at `~/projects/_shared/elementor-playbook.md`.
- `PAGES.md` records who owns which page. **Claim a page before you edit it.**
- `.mcp.json` holds the MCP connection. It contains no secrets.

## Setup

1. **Application Password:** on seniorhomesolutions.com go to WP Admin → Users → Profile → Application Passwords, name it "Claude Code", and copy the password.
2. **Auth token:** build it and add it to `~/.zshrc`. It's your own credential, so never commit it. Use `SHS_WP_AUTH`, not the Window Depot variable, so the two sites can't get crossed.

   ```bash
   echo -n 'your-wp-username:xxxx xxxx xxxx xxxx xxxx xxxx' | base64
   ```

   ```bash
   export SHS_WP_AUTH='<paste the base64 output>'
   ```

3. **Start Claude:** open a new terminal, `cd ~/projects/senior-home-solutions`, run `claude`, and approve the `shs-elementor` server when prompted.
4. **Angie consent:** if tools fail with an "external-scripts consent" error, approve it at https://seniorhomesolutions.com/wp-admin/admin.php?page=angie-app

## Workflow

1. `git pull`, then claim your page in `PAGES.md`, commit and push.
2. Build the page as a **draft** with Claude.
3. Review it while logged into WordPress.
4. Publish yourself after review. Update `PAGES.md` and add anything new you learned to `CLAUDE.md`. Put lessons that apply to any site in the shared playbook.
