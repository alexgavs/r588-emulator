# R588 Parking Logic — emulator

Interactive demo of how the **Samsonix R588** dash camera should behave in parking mode:
power (B+), ignition (ACC), parking timer and G-sensor, with the spoken Hebrew prompts
and the recorder showing which clips are written to which folder.

**Live:** https://alexgavs.github.io/r588-emulator/

- **B+** powers the camera. **ACC** only selects driving vs parking.
- Every mode change is announced once, so the driver hears which mode engaged.
- `ACC ON` → מצב נסיעה (driving mode) · `ACC OFF` → מצב חניה (parking mode, always)
- Parking timer on → adds צילום בחניה פועל (parking recording active), time-lapse to `Parking/F+R`
- Parking timer off → says "parking mode" and sleeps, still impact-armed
- Any G-sensor impact → beep + a protected clip in `Event/F+R`, in every mode

Single self-contained `index.html` (audio embedded).
