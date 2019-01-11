# AutoHotkey-Midi

Add MIDI input event handling to your AutoHotkey scripts


# About this folk

- open/close midi device by name
- passing ignored events to another device

---


```ahk

#include AutoHotkey-Midi/Midi.ahk

midi := new Midi( "Midi In Device Name", "Midi Out Device Name to pass" )

Return

MidiNoteOnA4:
	MsgBox You played note A4!
	Return

MidiControlChange1:
	cc := midi.MidiIn()
	ccValue := cc.value
	MsgBox You set the mod wheel to %ccValue%
	Return

```

## Requirements

* A modern version of AutoHotKey (1.1+) from http://ahkscript.org/
* A system with winmm.dll (Windows 2000 or greater)

## License

BSD

## TODO

* Documentation!
* Midi output event support
