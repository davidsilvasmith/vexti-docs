This is for Vexti Coding Standards.

They will most likely follow the wisdom in books like

- [https://www.amazon.com/Code-Complete-Practical-Handbook-Construction/dp/0735619670](Code Complete)
- [https://www.amazon.com/Pragmatic-Programmer-Journeyman-Master/dp/B003GCTQAE](The Pragmatic Programmer: From Journeyman to Master ) 

Short version:

1) Keep Code [DRY](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself)
2) The perfect is the enemy of the good - if an edge case seems hard keep moving forward, get the base case working and file an issue in the project's tracking system to have someone address through business requirements, budget, or refactoring.
3) Keep checkins to the point - don't check in random things - if a checkin says "fixes production bug when db is unavailable" there shouldn't be unrelated changes in there. This makes it easy to spot errors and roll back code if necessary.
4) If you see something wrong / broken and you can fix it in 5-15 minutes then do it. If not put an issue into the project tracker or email the project manager.