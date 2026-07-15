# Linked List Lab

A single-file, interactive teaching tool for singly linked lists. No build step, no dependencies — just one `index.html`.

## What it does

- **`New = Node(e)`** — type a value, click the button, a node box appears (data cell | next cell, defaulting to `None`).
- **`head = New`**, **`prev = New`**, **`curr = head`** — one click creates and moves the corresponding pointer flag onto a node, with a little slide animation.
- **`prev.next = New`** — links two nodes with a curved arrow, or drag directly from a node's right-hand ("next") box onto another node to do the same thing by hand. Drag it onto empty space to reset it to `None`.
- **`curr = curr.next`** — steps a pointer flag one link forward, animated, exactly mirroring the code.
- **Custom pointers** — add pointers with any name (`runner`, `slow`, `fast`, ...) for two-pointer / cycle-detection lessons. Drag them onto any node.
- Every action is logged live in the right-hand **console.py** panel as real-looking Python, so students see code and picture update together.
- Nodes and flags can both be dragged freely to rearrange the diagram for a slide or a screenshot.

## Deploying to GitHub Pages

1. Create a new repository (or use an existing one), e.g. `linked-list-lab`.
2. Add this `index.html` to the repository root (this README is optional).
3. Push to GitHub.
4. In the repo, go to **Settings → Pages**, set **Source** to `Deploy from a branch`, branch `main`, folder `/ (root)`, and save.
5. Your site will be live at `https://<your-username>.github.io/<repo-name>/` within a minute or two.

## Local preview

Just open `index.html` directly in a browser — everything runs client-side, no server needed.

## Customizing

Everything lives in the one HTML file:
- Colors and fonts are CSS variables at the top of the `<style>` block (`--head`, `--curr`, `--prev`, `--trace`, etc.).
- The reference `class Node` snippet at the top of the console panel is static HTML in the `.reference` div — edit it if you teach a different constructor signature.
- Default pointer names/colors are set in the `COLOR_MAP` object in the `<script>` block.
