# Desynchronized Days

Experimental VCMI engine and Simturns mod for a protected desynchronized phase: players advance using local clocks before synchronizing.

## Windows download

Download `desynchronized-days-windows.zip` from this repository's Releases page and extract it into a separate folder. This package is the existing Windows runtime, not a new build. It requires your own legally obtained Heroes of Might and Magic III game data, configured for VCMI.

## Configuration

The mod still uses the internal name **Simturns**. Its configuration is `Mods/simturns/Content/config/simturns.json`:

```json
{
  "desynchronizedDays": 14
}
```

The current configuration is **14 days**. The accompanying engine reads this parameter when configuring simultaneous turns. Enable the Simturns mod and select the weekly simultaneous turns option in game setup.

This requires the modified engine supplied here; copying the small Simturns content folder alone into a standard VCMI installation does not supply the engine changes.

## Sources and provenance

This repository contains a source snapshot from the local `vcmi-pr-weekly-simturns` checkout, commit `95830fed1`, with the runtime's Simturns documentation included. That checkout also contains Heroes3X and Magic Wands changes. The Windows release is preserved from the existing `vcmi-pr-weekly-simturns-runtime` directory; it has not been rebuilt or newly gameplay-tested for this publication.

VCMI is developed by the [VCMI project](https://github.com/vcmi/vcmi). Original authorship and licensing are preserved in `AUTHORS.h` and `license.txt`. See `docs/developers/` for build instructions.

## Prototype limitations

See `Mods/simturns/docs/time-event-scope.md` for deferred handling of scenario date conditions, quests, and timed map or town events during the desynchronized phase.
