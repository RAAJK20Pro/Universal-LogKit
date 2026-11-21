# Universal LogKit

A small root module that quietly keeps your phone's logs, so when something goes
wrong you have what you need to report it.

## What it does

- Keeps kernel, ROM and crash logs from every boot.
- Notes battery drain, deep sleep, heat and UI smoothness while you use the phone.
- Saves the last boot's logs by itself after a crash or a sudden restart.
- Tap **Action** in your root manager to save everything as three zips.

## The zips

| Zip | Contents |
| --- | --- |
| `Kernel_<time>.zip` | kernel log, performance and battery data |
| `ROM_<time>.zip` | Android logs (logcat, events, frame stats) |
| `Crash_<time>.zip` | tombstones, ANRs and crash logs |

Each zip has a `Summary.txt` that sorts what it found into
**Device**, **Health**, **Findings** and **Zips**. Findings are grouped by
where the problem is: kernel, ROM and apps, or battery and heat.

## Use

1. Flash the zip in Magisk, KernelSU or APatch and reboot.
2. Use the phone as usual.
3. When something feels wrong, note the time and tap **Action**.
4. Send all three zips.

## Notes

- Root is needed. Nothing is uploaded; the zips stay on your phone.
