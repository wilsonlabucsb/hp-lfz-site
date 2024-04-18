# Issues and Fixes

This page is intended to serve as a FAQ of sorts, so that users can find answers if they are experiencing a known issue.

---

Issue: Shaft vibrates when rotating.

Solution: Lubricate the length of the translator shaft with MoS$_2$ - grab a small vial and pour in a small amount of MoS$_2$ powder. Add some IPA or EtOH to create a suspension and sonicate to mix.

---

Issue: Shaft is fully retracted into the translator housing.

Solution: You will need to take off the rear flange from the opposite end of the translator. This involves undoing the large four bolts that hold the cone and thread seal and lock the dead flange in place. Be very careful to do the untightening evenly, as to keep the force on the cone-shaped sealing surface relatively balanced. As the flange begins to loosen, pull it away from the cone-shaped sealing surface as any scratches to this surface will cause a very expensive leak. You can use a long thin object (like a wooden dowel) to push the shaft back up and out into its normal position. If you have trouble getting the shaft to line up with the bearing holder (which should have a tight tolerance), you can use another thin, long object from the other end of the translator to try to nudge the shaft into the center of the bearing so it can pass through.

---

Issue: Shaft has disconnected from magnet pack

Solution: Send it back to SciDre for repair.

---

Issue: Shaft does not translate smoothly but gets stuck as it moves.

Solution: Similar to the issue of vibration during shaft rotation - need to lubricate the shaft with MoS$_2$.

---

Issue: Chamber repeatedly leaks at the seal rings.

Solution: If this issue persists even after replacing with fresh sesal rings, check the alignment of the Inconel adapters with the chamber. You can do this using a straightedge up against the sides of the adapter/chamber where the sealing surfaces meet, or by attempting to slide a piece of weigh paper in the gap between the adapter and chamber in an attempt to feel if the gap is bigger on one side more than another. Either the adapter is not mounted straight onto the translator, or the entire translator+adapter assembly is not mounted coaxial with the chamber. Remounting of these parts may be necessary.

---

Issue: The lasers are not communicating, they sometimes disconnect, or the LabVIEW software is stuck at the "read values" step.

Solution: Try restarting the LabVIEW software. See instructions on how to do this in the "Using the Lasers" SOP.

---

Issue: I tried to do automatic translation and the shaft moved as if I touched the fast gear button, even though the speed I had set for the automatic mode was slow.

Solution: This is a known bug in the translator software. This occurs if you use the "2-finger touch trick" to hold down the fast gear button (without having to hold your finger there the whole time), and if your next action is to enable automatic translation. The key is to do an intermediate step before enabling automatic translation. For example, after using the "2-finger touch trick", you should arbitrarily press any +/- key to change the automatic translation speed (you can, for example add 0.1 mm/hr and then subtract 0.1 mm/hr). Now, because there was some intermediate action, you should have no problem enabling the automatic mode. In any case, it is safest to turn on automatic translation in a "harmless" direction. For example, begin translating the seed downwards or the feed upwards, so that you don't accidentally crash the feed and seed into each other if you run into this bug. The worst that could happen is that this bug appears and they move unexpectedly fast, but in a safe direction.

---

Issue: The logfile prompt on the LabVIEW software is not appearing / the lasers are not responding or connecting to PC2.

Solution: If none of the lasers are successfully communicating with PC2, try restarting the Netgear box by unplugging its power supply and then reconnecting. If that doesn't work, try verifying that each individual laser is working correctly by directly connecting an ethernet cable between the computer and ONE laser and try pinging that laser's IP address from the command prompt using "ping 192.168.3.23X" where X is the laser number.
