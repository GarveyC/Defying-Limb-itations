This script was developed as part of my undergraduate research project:
"Defying Limb-itations: Revolutionising Accessible Prosthetics Through 3D Printing."

It automates the creation of mirrored prosthetic moulds from 3D scans of forearms/stumps, using open-source tools and Python-based mesh processing.

🧠 What It Does
This tool:

Loads a 3D STL model of a prosthetic forearm and a scanned stump

Repairs the meshes to make them watertight

Mirrors the prosthetic model across the X-axis

Adds a custom padding factor to the stump model (to allow for socket clearance)

Uses a Boolean subtraction to generate a mould:
Mirrored Forearm – Padded Stump

Saves the result as a new .stl file ready for 3D printing



📁 Input Files
mirrored_forearm.stl — the prosthetic design you want to mirror

scanned_stump.stl — 3D scan of the user’s residual limb
(ideally aligned and cleaned beforehand)

📤 Output
mirrored_mould_with_padding.stl — the ready-to-print mould file, subtracting the padded stump from the mirrored forearm.


⚠️ Known Limitation
There’s currently an unresolved bug in the Boolean subtraction step, especially with certain mesh configurations.
If you're experienced with trimesh or mesh boolean ops, I'd love your input!
