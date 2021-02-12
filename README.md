# kvm
An open-source HDMI Keyboard/Video/Mouse (KVM) switch, which lets you switch two monitors and four USB devices between up to three computers. Theoretically, it should support HDMI 1.3a and up to 1920 x 1200 resolution, but that's completely untested and probably depends on how well I actually designed the board.

The base has a total of six HDMI inputs (three computers with two monitors each) and two HDMI outputs (for the two monitors). It also has four mini-USB ports (three computers and one for power), four USB host ports (to connect a mouse, keyboard, and anything else), and a connector that goes to the keypad.

The keypad has a 3x3 grid of buttons. Pressing the buttons lets you switch monitor 1, monitor 2, and the USB ports between the three computers. It connects to the base via a cable, and receives power over that connection.

A [PS/2 connector](https://en.wikipedia.org/wiki/PS/2_port) and cable is used between the base and keypad. **Importantly, neither device actually speaks the PS/2 protocol!** PS/2 was just chosen because connectors and cables are readily available. You should not connect either device to anything else with a PS/2 port, or any sort of PS/2 adapter. (you most likely won't break anything, but it definitely won't work)

The source code/files are split up over several different repositories:
* [kvm-base](https://github.com/thatoddmailbox/kvm-base) - The main switch, with all input/output ports, and a connector that goes to the keypad.
* [kvm-keypad](https://github.com/thatoddmailbox/kvm-keypad) - The keypad, used to select the state of the various switches. Connected to the base.
* [kvm-fw](https://github.com/thatoddmailbox/kvm-fw) - The firmware that runs on both the base and the keypad.