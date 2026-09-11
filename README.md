# friends.hanzo.ai

One file: the friends and family deck, sealed.

`index.html` carries the deck as AES-256-GCM ciphertext. The key is the password
readers are given, derived with PBKDF2-SHA-256 over 600,000 rounds; a wrong
password yields nothing to look at, because GCM refuses rather than returning
plausible bytes. What travels in the clear is the shell — the two faces, the
stylesheet, the gate and the top bar, so a reader can set the colour before
typing — which tells you the deck exists and what four links are called, and
nothing about what it says.

Published from `hanzoai/deck`, which holds the deck itself, the rail, the sealer
and the data room. Nothing is edited here — a push overwrites it.
