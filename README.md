# Pygmy

This project is a rocket flight computer design for my TRA L1 certification flight. The name is a play on the fact that
it's designed to be small and also runs on a Pi (Py) chip. Yes, that means you can program it with MicroPython (Py).

![Pygmy Rev A](./docs/assets/pygmy.png)

The flight computer also has a sibling ground station receiver, the Pygmy GS.

![PygmyGS Rev A](./docs/assets/pygmy-gs.png)

## Motivation

I am a computer systems engineer who has designed avionics for my university's rocketry team for several years. I like
the challenge of designing, building and programming embedded systems for unique environments, like the inside of a
rocket. Although my L1 flight won't have the same challenges as my university's rockets (which fly up to 30k feet and
have hit Mach 1.89), it will still have challenges. It is, differently, entirely my own design to mess with and do as I
please!

My L1, as far as I'm concerned, is to be a relatively standard L1 rocket build (not a kit, still my own) outside of this
flight computer. That way I can get my cert while having a rocket which meets my primary goal: being a vessel for my
flight computer.

## Usage

To learn how to use the Pygmy, please check the manual under the `docs/` sub-directory. This manual contains both the
user guide for operation and a detailed developer guide.

Both guides are currently under construction.

## Other Goodies

Along with the Pygmy and PygmyGS E-CAD design files _and_ free, open-source software, there is additionally parametric
CAD enclosure designs included in this repository.

The PygmyGS case can be found under [`ground-station/enclosure`](./ground-station/enclosure), along with an assembly
file so you can see the PygmyGS mounted inside it with all the fasteners.

A sample avionics bay for the Pygmy flight computer can be found under
[`flight-computer/enclosure`](./flight-computer/enclosure), along with an assembly file so you can see the Pygmy mounted
in the bay with a battery and arming switch. This design is also fully parametric so you can modify it to the body tube
diameter of your rocket, different battery size, etc. This design is largely based off of the configuration I flew in my
L1 certification flight, so feel free to fully change it depending on your constraints and desires! It is by no way the
recommended configuration for the Pygmy, just one possible design.
