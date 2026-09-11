# Media

Git är bra på text och dåligt på stora filer. Regler:

- **Bild:** JPG/PNG/WebP, längsta sida 2048 px, max ~5 MB. Namn: `YYYY-MM-DD-the-lab-practica-01.jpg`.
- **Video:** MP4 (H.264), max ~50 MB per fil här; original och långa klipp ligger i Drive-mappen *Usha – Marknadsföring/media* och länkas i `media/video/INDEX.md`.
- **Ljud:** MP3/M4A för lyssning, WAV bara om det ska mixas. Voice-over-manus i `media/text/`.
- **Text:** manus, transkript (`.md`), undertexter (`.srt`).
- **Samtycke:** filnamn med `-consent` betyder att alla identifierbara personer sagt ja. Utan det: lägg inte upp.
- Git LFS är inte installerat på arbetsdatorn. Behövs det (många videor): `brew install git-lfs && git lfs install && git lfs track "*.mp4"`.

Index per mapp (`INDEX.md`) listar vad som finns, var originalet ligger och vilket inlägg det användes i.
