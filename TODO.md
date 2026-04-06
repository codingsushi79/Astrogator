# TODO

## Done (see recent commits / changelog)

- Allow a window of times for transfers — bounded outer search, earliest-UT filter, fudge on bisection bounds, legacy fallback cap (no infinite loop)
- Merge the correction burn into the ejection burn — optional setting; combines plane match at ejection with Hohmann prograde in one node
- Re-do launch approximation — refined atmosphere term on `DeltaVToOrbit` (coarse model; further tuning welcome)
- Localization: mid-sentence body names — `DisplayNameMidSentence` strips leading English “The ” for labels like planet column / subtitles
- Vessel destruction / rails / orbit spam — `onVesselDestroy` reload when origin lost; `onVesselGoOffRails` / `onVesselGoOnRails`; throttled orbit reload to mitigate set-orbit cheat stalls
- Probe / CommNet — translation node adjustments skipped when `connection` reports disconnected (avoids bad interaction)
- Keys with nested encounter — `ActiveTransfer` prefers the row matching current `VesselTarget`
- RasterPropMonitor — path mode line on MFD; `buttonPathMode` / `buttonCycleAssistMoon` (defaults 7 & 8); see `AstrogatorRPM.cfg` comments

## Code style (still open)

- Generalize retrograde orbit special cases
- Split ViewTools: Truly generic stuff versus this project's stuff
- Split MathTools off from PhysicsTools
- Factor out a SimpleMod base class
  - App launcher button
    - Tooltip
  - Main window
  - Settings
  - Resources
  - Event handlers
- Implement [TaxiService's method of updating the UI without close/reopen](http://forum.kerbalspaceprogram.com/index.php?/topic/149324-popupdialog-and-the-dialoggui-classes/&do=findComment&comment=2950891)
- Unit tests

## Deferred pending stock changes

- Rendezvous with asteroids near Pe of their future encounter/escape trajectories
