# MatchlockAshigaru
Include: dynamixel AX-12A program, Bluetooth Commander app and PS3 controller USB Host
![Matchlock](https://github.com/huyle10/MatchlockAshigaru/blob/master/Matchlock/matchlock.jpg)

## Inverse Kinematics function in nuke.cpp

*To turn this into progamming language, you’ll have to remember that the angles are unknown, and we need to work it out using equations and trigonometry.

![Graphical Presentation](https://github.com/RemembralI/MatchlockAshigaru/blob/master/Matchlock/160120121365.jpg)
![Matchlock Graphics](https://github.com/RemembralI/MatchlockAshigaru/blob/master/Matchlock/leg-planes.jpg)

**So, first thing is going to be simplify this problem from 3D into two 2D problems, to solve for α (alpha), β (beta) and γ (gamma). 
![2D Graph](https://github.com/RemembralI/MatchlockAshigaru/blob/master/Matchlock/2-IK-side1.jpg)

**Gamma is easy, from the 2D diagram, we have:
![GammaFunction](https://github.com/RemembralI/MatchlockAshigaru/blob/master/Matchlock/3-gamma.jpg)

**Alpha is a bit tricky, so I tend to split it into Alpha1 and Alpha2. We can get Alpha1 by working out L first.
![Alpha1Function](https://github.com/RemembralI/MatchlockAshigaru/blob/master/Matchlock/11.jpg)
![Alpha2Function](https://github.com/RemembralI/MatchlockAshigaru/blob/master/Matchlock/61.jpg)

*Cosine Rule!
![CosineRule](https://github.com/RemembralI/MatchlockAshigaru/blob/master/Matchlock/Cosine_Rule.gif)

From these formula, if we know 3 sides of a triangle, we can find out any angles inside it. Don’t doubt it, it just works! :-)
So now we have Alpha2,
![Alpha2](https://github.com/RemembralI/MatchlockAshigaru/blob/master/Matchlock/71.jpg)

Alpha1
![Alpha1](https://github.com/RemembralI/MatchlockAshigaru/blob/master/Matchlock/81.jpg)

A little spreedsheet to speed things up
![IKspreadsheet](https://github.com/RemembralI/MatchlockAshigaru/blob/master/Matchlock/Inverse%20Kinetics%20Chart.PNG)

#References:
<http://blog.oscarliang.net/robot-forum-archive/>
