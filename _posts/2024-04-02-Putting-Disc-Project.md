## Dead Zero Putting Disk

### Premise
My dad designed a golf training aid a number of years ago called the [Dead Zero Putting Disk](http://deadzeroputting.com). The premise is simple: if your putt hits the disk at an appropriate speed, it would have gone in the hole. "Appropriate speed" is the key phrase here. Dave Pelz, a well-known golf instructor, claimed that the optimal speed for a putt would see the ball stop no more than 17 inches past the hole if it missed. The logic is that the putt needs to be going slow enough to fall into the hole if it catches the lip.

The putting disk is sized such that a putt of optimal speed will make contact with the disk, but there is no way to know if the speed is actually optimal. My dad was discussing the design with a friend recently who suggested integrating an accelerometer to evaluate the impact. Theoretically, an impact above a certain magnitude could be detected and reported to the user as too firm. 

### Business Applications

Knowing the economics of making these putting disks, I don't think the accelerometer adds enough value to justify its cost. This is especially true  considering that the end result would involve several more manufacturing steps and developing an app. However, because I can work for free for my dad, I still think it will be a unique problem to solve. If the prototype works exceptionally well, perhaps there's a market for golf instructors to buy a disk for students to use in their training sessions.

### Methodology

Initially, I figured I should do some test impacts with the accelerometer on the disk and then calculate a decision envelope that would classify impacts as "too firm" or "just right." After checking out the data stream from the device, I realized there were far too many features to manually create an accurate decision boundary. It became immediately obvious that I should train a model to classify impacts instead. It would be a great data science project with real world applications, even if the device remains a prototype.