# msxl
Mono Sequencer XL

ISSUE ITEMS
===========

- [ ] VARIANT: Wenn schnell hintereinander DUPLICATE > HÄNGER. Vielleicht delay am Anfang oder deactive button bis the duplicate aktion abgeschlossen ist.
- [ ] CONTROL: Exec löst keine Änderung für Move am Target aus. CHECK
- [ ] CONTROL: Step/Slot im HOVER einzeigen
- [ ] CONTROL: Erweiterung auf 128 Schritte ? Link mit zweitem live.grid. DARSTELLUNG: Stacked mit Follow On oder LEFT X-1/RIGHT 1  
- [ ] Die restlichen TOOLBARS anpassen wir bei PITCH. [PV FETCHED]!
- [ ] Wenn DEVICE geladen wird, werden die Defaults nicht all gesetzt und auch nicht das initiale PATTERN 1.
- [ ] Es wird DISPLAY_SEQ und TARGET_SEQ mit jedem Step geschickt => PERFORMANCE
- [ ] TOOLBAR (PITCH): Pitch auf 60, erster Drück auf Randomize setzt nur ersten Step. Zweiter Drück randomisiert.
- [ ] CONTROL: Step status TEXT (haken/kreuz) wird nicht angezeigt
- [ ] MAKENOTE: Note wird gespielt, obwohl Transport aus ist. Gate zu MAKENOTE hinzugefügt.
- [ ] CONTROL: Value in overlay anzeigen
- [x] VARIANCE: Pitch: variance is sometime set to MAX which is 12.
- [X] FIXME: Generate random pitches not working > REWRITTEN and part of toolbar
- [ ] Edit To does nothing if step is moved
- [x] FIXME: Conform to scale in Pitch inserts at wrong step index
- [x] FIXME: Tabwechsel bei Pitch ändert Tonlage
- [x] FIXME: Die Ansicht ist noch nicht korrekt. Ist 60-84 muss aber 48-62 sein
- [x] FIXME: Zusätliche Parameter für Map1 und Map2 in DICT einbauen
- [x] FIXME: Wenn man auf Subtab wechsel durchführt ändert sich die pitch view von anderen MS devices. GLOBAL?
- [x] FIXED: Bei Wechsel Steps wird diese Anpassung bei Pitch nicht nachgezogen. Vermutlich ein extra1 Problem.
- [x] FIXME: MAP1: Direction funktioniert nicht
- [x] Pulse devision not yet working correctly. Steps sometimes >1. Changed calculation of timing to FLOAT. Bug in original Mono Sequencers of [generate_note]
- [x] Load a pattern is slow. see below.
- [x] Super high CPU load. Every vars in the modulators are always stored and what not. Added a change element to avoid dublicates so only changed values will be stored
- [x] Loading pattern from storage not loading into UI. Changed to [preset] as storage
- [x] Pulse Multiplication not working due recognizing to _Transport_ status
- [x] Changing values especially the slider are slow if need MSXL.storage.key is used.
- [x] Fly-out changes with switching the pattern.
- [x] dict ---mseq getting reset for unknown reason. OBSOLETE. Chnaged to preset object.
- [x] generate_note generates multiple notes in one step. How comes!
- [x] live.text doesn't understand activecolor, activetricolor2
- [X] MIDI IN Notes are always forwarded. Where is this coming from? REMOVED SOME ALIEN CODE
- [X] Chance and Variance not reset to default. DEFAULTS DEFINED FOR TOOLBAR AND RESET WITHIN TOOLBAR
- [x] Loopedit not set at the beginning. ADD: pattrn object
- [x] Pulse not in sync with step lane (1 pulse behind) due to msxl.counterx --r_puls input from outside leading to slight delay. --r_pulse now used within patcher. inlet obsolete. Made ---r_pulse in step lanes counterx switcher as inlet
- [ ] PRESET SLOT: When recalled the preset is automatically stores > PERFORMACE > MOVE TO NON-AUTO-SAVE? GETEDIT = 0 ?
- [ ] 

DONE ITEMS
==========

- [ ] CONTROL: Store Slot Actions as **Favorite**.
- [x] CONTROL: Default value 
- [x] CONTROL: Chance for Slot Actions.
- [x] DONE: Langsameren Main Pulse als Whole Note einbauen: 1n, 2n ... 32n
- [x] Modulation: Put CC and Ableton modulation on one single, reusable view with switcher 
- [x] Add 2 additonal CC targets (6  in total)
- [x] Reusable parameter setting/retrieval as abstraction (msxl.storage)
- [x] Reqork housekeeping so that keys are determined automatically
- [x] Introduce _dict ---pattern_ to hold the current pattern data.
- [x] Modulation view as abstraction for better reusability in all lanes
- [x] Added keyboard to show notes from sequencer.
- [ ] Step through via buttons
- [ ] MIDI input taken for step wise editing. Automatically moves to next step.
- [x] Add **pulse control** to all Lanes
- [x] Modulation for all lanes
- [x] Snippets: To Snippet Manager OK. To Pattern OK. Naming OK.😄
- [ ] Snippets: 6 Categories (SOLUTION: Dump out and Import e.g. DICT or PATTR object)
- [ ] Snippets: Copy duration lane to the right target duration lane.
- [ ] Snippets: Save to file. Global dict is not working with multipe MSXL. ⚠️
- [x] Global Copy/Paste: of Lanes working. 
- [ ] Global Copy/Paste: copy also the information stored in preset object.
- [x] Sync mode for loop points (pitch)
- [x] RESET PATTERN/ALL: reset all 64 steps. CODE ADAPTED.
- [X] SCALE: Conform to scale rewritten and new scales. REWRITTEN.
- [X] Fold mode for pitch sequencer added
- [X] Small keyboard showing scale + active step
- [X] Large keyboard added below pitch sequence. Show/hide toggle added.
- [ ] Restart sequencees after changing looping points. Make this configurable ?

OPEN
====

- [ ] CONTROL: Favorite Actions > Add to Action Register. Make available in Lanes
- [x] CONTROL > Steps: 1:+/-n ändert Step um entsprechenden Wert
- [ ] Teste Abstraction vom gesamten MSXL. Mal sehen was passiert.
- [ ] RUN/EDIT MODE: Während eine Pattern Seq läuft kann eine weitere bearbeitet werden. Dann wechsel.
- [ ] CONTROL: Farben für Targets.  
- [ ] VARIANTS: 3x17 variants can be created. 64 are technically possible. Manual selection. Variant 1 is default.
- [ ] MAGNET MODE: All linked devices are vertically grouped and aligned in floating window state.
- [ ] LINKED MODE: Foward transposition to slaves
- [ ] Remove --r_pulse input parameter from msxl.counterx and add 0|1 switch to patcher (is this really needed?)
- [ ] Save CONTROL action into global repository and add exec menu to toolbar.
- [ ] Choose CONTROL STEP via MIDI CC or Note. Define START and END
- [ ] Add **VARIANT CHOOSER to every LANE** so that the user or CONTROL SEQUENCER can change it individually. With PATTERN SETTING the VARIANT is set for all lanes.
- [ ] VARIANT: Change variant via MIDI Note or CC. Add to MIDI Menu "Variant"
- [x] Go from dict model to preset model because of performance issues and it is easier to handle.
- [x] Change parameter storage to MSXL.storage. **OBSOLETE**

- [x] Use _MSXL_ as prefix
- [ ] Step manipulation toolbar to be generic and reusable in all lanes
- [ ] _Sustain mode_ for Pitch Lane
- [ ] _Sustain mode_ per Step
- [ ] _Chance/Deviation_ for all lanes
- [ ] ONGOING: _Control Sequencer Lane_ to control other lanes.
- [ ] add ---save to all vars to update changes immediatelly. **IS THAT A GOOD IDEA**?
- [ ] Change Modulation Lanes to 64 steps by default.
- [ ] **Remove all the junk** :exclamation:
- [x] MSXL.s and MSXL.r as a replacment for send/receive but with postfix to be used in interdevice exchange or using multiple instances of a patcher within the device
- [x] Main UI components now grouped nicely in bpatchers
- [ ] Sync the Loop Points and steps of all lanes (Configurable)
- [x] SNIPPETS: Sync of snippets across all MSXL (using external global dict)
- [ ] SNIPPETS: Replace snippet snyc: Global send seq message together with device id. Receipients filter for master and update their pattr object
- [X] FIXED SNIPPETS: If snippet name is changed, the menus are not rebuild.
- [ ] LINKED MODE: Transpose to be synced. 1st device in chain is master.
- [ ] All lanes can have a different step count but can be synced with global step count. 
- [ ] GLOBAL PULSE: Add a constan delay to the midi note.

IDEAS
=====

- [ ] Lock Looppoints to step lane. dfgff
- [ ] 8 Variants per pitch pattern: Pitch sequence stays same, variante, e.g repeat my vary. Can be choosen in Control Lane.
- [ ] Hocketing for 4(?) Midi devices
- [ ] Import MIDI file
- [ ] Drag / Drop to and from Ableton
- [ ] Import Midi to Snippet Manager
- [ ] ⭐ Sync Mode: Sync multiples instances with one master to create something like e.g. Fugue
- [ ] IDEA: _Strum Lanes_ 👍
- [ ] IDEA: Bend lane 👎
- [ ] IDEA: Programs = Pattern chains + program chains :heart:
- [ ] IDEA: Save pattern as Default
- [ ] ~~IDEA: Devider für Lanes Velocity, Dura, Octave, Parameter, program~~
- [ ] IDEA: Poly version of Pitch Lane with a Matrix
- [ ] IDEA: Separate window view where you can change the layout, so that all lanes can be visible at once :heart:
- [ ] IDEA: 2 additional Modulation Lanes
- [ ] IDEA: More scales
- [ ] IDEA: Folded scale view in Pitch Lane
- [x] Multiple Play Heads: Devices can be linked. 1 Master Multiple slaves. Working for pitch lane. Works across tracks.
- [ ] Poly Version
