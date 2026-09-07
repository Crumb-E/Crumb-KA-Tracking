# Weeks 3-4
Decided to start jotting down progress on a day to day basis because putting the theory into my own words helps, and just because I want to.

### Monday
Was busy shopping and cooking today. So I decided to just read until reaching the point of writing code and return to that tomorrow.

Tutorial got into explaining the graphics pipeline. I've messed with shaders before but it was a sort of magic "black box" situation where I didn't really get the logic behind it. It's cool starting to wrap my head around the actual logic to it.

Some takeaways from what I read I wanted to write down.
- Early on it was stated OpenGL is like one big state machine which I am starting to get with the logic of OpenGL "hints" functionally being like state changes for handling different types of data.
- Similar to UV mapping, Bresenham's line algorithm, and some other assorted things I've worked with before. It seems there's a trend of normalizing vectors to represent handling arbitrary forms of distance. As in. Before being rasterized (mapped to pixels e.g. 1920x1080) data is often mapped on a scale of 0-1. Then due to math and algorithmic magic we can map these to pixels. I know this from the line algorithm which is how we get an array of pixels that lines up with a... line. I always wondered how mapping to different resolutions work and this seems to be related. You just pass a different number in and it adapts it.
- "Fragments" are OpenGLs term for pixels. Or rather the data related to drawing a pixel. There's a lot more in it then you'd think. Like lighting data. It's strange to think a 2d pixel needs that much data but it's interesting too. Also makes more sense as I read about the pipeline.
- Fragments can overlap. Despite being a 2d array of pixels they have a value for "depth" that determines whether to be discareded, or if transparency is involved blended together. This has made me think about a lot of optimization stuff I've looked into before. A famous example is Minecraft improving performance with surface culling. Predicting surfaces that cannot possibly be seen and not rendering them to save time. Related here, in that I assume it would translate to not having to run the shaders on those pixels due to already knowing they cannot be rendered. From memory another technique is discarding surfaces that are facing away from the camera/viewport.
- In general, as I am super into video games, and animation, and modelling. Relating my other knowledge to this is actually quite fun to me. It's satisfying to understand the underlying logic behind things.

When I told my dad about my goal of a benchmark renderer he got excited about it with me and we talked about rendering tech for a bit. Also he offered to model a custom benchmark scene to test importing blender models. So that is now an addition I am wanting to add in.

One thing I have heard repeatedly is making the first triangle is them major hurdle. Well, the tutorial seems to be backing up these claims.

![Tutorial excerpt saying making triangles is hard bro.](Media/CrumDoc-2-1.png)
