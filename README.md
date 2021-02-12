# kvm
An open-source Keyboard/Video/Mouse (KVM) switch. Has support for two monitors and up to three computers.

The source code/files are split up over several different repositories:
* [kvm-base](https://github.com/thatoddmailbox/kvm-base) - The main switch, with all input/output ports, and a connector that goes to the keypad.
* [kvm-keypad](https://github.com/thatoddmailbox/kvm-keypad) - The keypad, used to select the state of the various switches. Connected to the base.
* [kvm-fw](https://github.com/thatoddmailbox/kvm-fw) - The firmware that runs on both the base and the keypad.