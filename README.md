# bardachd-docs

The privacy policy and support page for **Bàrdachd**, published as web pages
because App Store Connect requires both as *URLs* and will not accept the app
without them.

Same arrangement as `fonn-docs` and `Orain`.

## Why this is a separate repo

The app's own repository is private — it sits inside the Raspberry Pi project,
which carries the Pi's Tailscale Funnel address and home LAN addresses. GitHub
Pages on a private repository needs GitHub Pro; a second public repository
costs nothing, and has the side benefit that the only thing ever public is two
documents written to be read by strangers.

## One copy, not two

`fonn-docs` keeps its originals in `~/Ceol/docs/` and copies them across, and
its own README warns that keeping two originals in step by hand is how they
come to disagree. That warning turned out to be right: the local copy of the
Fonn privacy policy and the published one now give different contact
addresses.

So this folder is the only copy. Edit here, commit here. There is nothing to
keep in step.

## Publishing it

1. Create a **public** repo called `bardachd-docs` on GitHub.
2. Push this folder to it.
3. Settings → Pages → Source: *Deploy from a branch*, branch `main`, folder
   `/ (root)`. Save.
4. Wait a minute or two, then check both pages load in a private browsing
   window — the point is that they work for someone who is not signed in:

   - `https://glenachulish.github.io/bardachd-docs/privacy`
   - `https://glenachulish.github.io/bardachd-docs/support`

5. Put those two URLs into App Store Connect: *Privacy Policy URL* on the App
   Privacy page, *Support URL* on the version's App Information page.

## When the app changes

If Bàrdachd ever starts collecting anything, sending anything, or asking for a
permission, `privacy.md` is updated **before** that version ships, and the date
at the top changes. A policy that describes the last version is a false
statement about this one.

The claim that matters here is the strong one: the app never touches the
network. If that ever stops being true — a dictionary update fetched at
runtime, say, or anything that phones home — the policy has to change in the
same commit.
