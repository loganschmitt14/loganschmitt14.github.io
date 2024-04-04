## Dead Zero Putting Disk

### Premise
My dad designed a golf training aid a number of years ago called the [Dead Zero Putting Disk](http://deadzeroputting.com). The premise is simple: if your putt hits the disk at an appropriate speed, it would have gone in the hole. "Appropriate speed" is the key phrase here. Dave Pelz, a well-known golf instructor, claimed that the optimal speed for a putt would see the ball stop no more than 17 inches past the hole if it missed. The logic is that the putt needs to be going slow enough to fall into the hole if it catches the lip.

The putting disk is sized such that a putt of optimal speed will make contact with the disk, but there is no way to know if the speed is actually optimal. My dad was discussing the design with a friend recently who suggested integrating an accelerometer to evaluate the impact. Theoretically, an impact above a certain magnitude could be detected and reported to the user as too firm. 

### Business Applications

Knowing the economics of making these putting disks, I don't think the accelerometer adds enough value to justify its cost. This is especially true  considering that the end result would involve several more manufacturing steps and developing an app. However, because I can work for free for my dad, I still think it will be a unique problem to solve. If the prototype works exceptionally well, perhaps there's a market for golf instructors to buy a disk for students to use in their training sessions.

### Methodology

Initially, I figured I should do some test impacts with the accelerometer on the disk and then calculate a force threshold that would classify impacts as "too firm" or "just right." I had a number of concerns with this approach:  How could I correctly classify a glancing blow? Would I have to align accelerometer with the line of the putt for consistent readings? Would I need a second accelerometer to account for side blows?

I connected the device to my computer to check out the data stream. To my surprise, the accelerometer provides much more data than I anticipated. 

### Features here ### 

It became immediately obvious that I should train a model on these features to classify impacts instead. It would be a great data science project with real world applications, even if the device remains a prototype.

### Experimental Design

I need to collect training data for the model in such a way that I can add a binary classification feature for each impact. The data come in time series format, with a sampling rate of my choosing, so the first step in the process will be experimentally determining what type of collisions even register as a discernable impact and what sampling rate gives me the best resolution so I can create an impact processing filter. 

Once I create the processing filter, I can run the data collection trials. I'll use a ramp to roll the ball toward the disk, varying the release height to change the ball speed from an acceptable range to an excess range. I'll translate the disk across the ball's path to change where the ball impacts the disk. Finally, I'll also rotate the disk to change the incident angle of impact. My goal is to have a variety of impact conditions ranging from direct blows to glancing blows from every angle of incidence. I can then process the data to filter for impact events, add a binary feature for "acceptable impact," and train a model. I'm imagining the model creating some high-dimensional envelope that contains all acceptable impact conditions and excludes impacts that are associated with excess speed.

### Other Considerations

I think it would be trivial and could be a good idea to simply reject all impacts that register above a certain force value in any one direction. I'd determine the force of a square collision and auto-flag any of those impacts. I'm not sure if that will improve the performance or not.

I'm still not sure if the single-accelerometer approach will work. I'm hoping that a glancing blow will either generate some measurable rotation or distinct quaternion change that distinguishes them from a more square blow.

Finally, the accelerometer I'm using is larger than any device that would be integrated into a production version of the disk. As such, any model that is trained on this device would need to be retrained for a final version. As I don't expect the economics of the product to make much sense for a production run, I'm not so concerned about this. 