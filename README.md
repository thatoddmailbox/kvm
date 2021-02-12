# kvm
An open-source HDMI Keyboard/Video/Mouse (KVM) switch. Has support for two monitors and up to three computers.

The base has a total of six HDMI inputs (three computers with two monitors each) and two HDMI outputs (for the two monitors). It also has four mini-USB ports (three computers and one for power), four USB host ports (to connect a mouse, keyboard, and anything else), and a connector that goes to the keypad.

The source code/files are split up over several different repositories:
* [kvm-base](https://github.com/thatoddmailbox/kvm-base) - The main switch, with all input/output ports, and a connector that goes to the keypad.
* [kvm-keypad](https://github.com/thatoddmailbox/kvm-keypad) - The keypad, used to select the state of the various switches. Connected to the base.
* [kvm-fw](https://github.com/thatoddmailbox/kvm-fw) - The firmware that runs on both the base and the keypad.