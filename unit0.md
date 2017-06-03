# Unit

## Welcome to CSE 167x

> Welcome to Computer Graphics on EdX. I am Ravi Ramamoorthi, a
> Professor of Computer Science and Engineering at UC San Diego. In this
> 6 week course, we're going to learn the concepts of 3D computer
> graphics, and write programs to display 3-dimensional scenes with
> accurate lighting, using both real-time graphics in OpenGL and GLSL,
> as well as ray tracing. You will develop a real-time 3D scene viewer
> in homework 2, that renders scenes with lights and materials, allowing
> you to look at them from any direction, as well as to move and to
> scale the scene, making it bigger or smaller. In the process, you will
> be able to write interactive 3D programs in OpenGL and GLSL. The
> images here are a collage of some results produced for the final
> raytracing assignment in our local class a few years ago. You will be
> able to make images like these of 3D scenes with reflections and
> shadows for your final homework 3. We hope you will join us to learn
> about the magic of 3D computer graphics.


--

# L1V1: ONLINE GRAPHICS OVERVIEW: MOTIVATION

#### Unit 0 > Lecture 1: Course Overview > L1V1: ONLINE GRAPHICS OVERVIEW: MOTIVATION

## L1V1: Online Graphics Overview: Motivation

> Welcome to these online lectures for computer graphics. I am Ravi
> Ramamoorthi, a professor at the University of California at San Diego.
> Over the next several lecture segments, we are going to study some of
> the beauties of computer graphics, some of the ways in which 3D
> computer graphics are created and we will be doing some interesting
> assignments that will enable you to create your own computer graphics
> programs. Let me first say a little bit about myself, and then I'll
> talk a little bit about the course. I obtained my PhD from Stanford
> University in 2002, and my PhD thesis developed the methods of
> spherical harmonic lighting. Today you can do a Google search for
> spherical harmonic lighting and you'll find more than 50,000 hits.
> It's a technique that's very widely used today in 3D computer graphics
> and most recent video games, and many recent movies. It's also being
> used for example by Adobe for relighting images. I've included the
> link to my web site, if you want to know more about me and my work,
> you have links to several videos, several papers that may be of
> interest. After getting my PhD I spent 6.5 years at Columbia
> University. And then I taught for 5.5 years at UC Berkeley. Since July
> 2014, I've been at the University of California, San Diego, where I am
> the Director of the Center for Visual Computing. My research has
> focused on a variety of topics. It has included computer graphics
> image synthesis, how do you create realistic images: a process known
> as rendering, that's been my main area of interest. Also how do you
> acquire images from the real world, you start to create realistic
> visual appearance of objects. And broadly I've been interested in how
> do you simulate the realistic beauty and appearance of the natural
> world. I have been fortunate to receive a number of awards for my
> research work, including the ACM SIGGRAPH significant new researcher
> award in 2007, which is given to one young computer graphics
> researcher a year. I've included a link there to the video that was
> produced for my award. If you're interested in looking at that and
> getting an idea of the kinds of things I do, you're welcome to do so.
> I was also fortunate to be honored by the White House with the
> Presidential Early Career Award for Scientists and Engineers or PECASE
> award in 2008. Most relevant to these lectures, I've taught computer
> graphics at Stanford, Columbia, and the University of California. I've
> taught it a total of more than 10 times locally, and the course you're
> going to get is updated to cover the real basics of computer graphics
> and also to take advantage of recent developments, in particular we'll
> talk about graphics programming units, the use of programmable shaders
> and it's the course is really a modern introduction to many of the
> fundamental topics in 3D computer graphics. The goals of the course.
> So there are two main goals. First you need to be able to write
> systems. So this is really a course that teaches you how to program 3D
> computer graphics and write your own 3D graphics programs. So you will
> be writing both real-time graphics programs using OpenGL, which is a
> graphics API. And, the OpenGL shading language. In particular, you
> will be building a real time scene viewer. You will also develop
> programs off line for a technique known as ray tracing, which will
> enable you to create realistic images of 3D scenes. Along with the
> systems, the goal of the course is to understand the theory of
> computer graphics, and in particular the mathematical techniques and
> the algorithms that underlie most of modern 3D graphics systems. I
> should mention that this is not a course about the specifics of a
> particular 3D graphics programming environment like Maya, DirectX etc.
> However, in order to understand the concepts you will be writing
> programs and so you will have a great deal of facility in writing 3D
> graphics programs in Open GL and the GL shading language. This should
> be portable to other systems if you so desire at a later time. Let me
> give you a little bit of a hint of the kinds of things you'll be able
> to do in this course. This is a collage of the some of the images
> produced by the ray tracer when I taught this course 5 years ago. And
> if you look at the web sites for more recent instances of the local
> course at Berkeley, you can see other types of images that people have
> been able to produce. And you notice that these images show some of
> the beauties of 3D graphics and ray tracing. So you can see the nice
> reflections or refractions through the glass spheres. The way the
> chess pieces cause their reflections on the chess boards. And you can
> do all of this by the end of the course. The purpose of this initial
> segment is to also motivate you and so one of the questions is why do
> we study 3D computer graphics? And for 2 real reasons, one is there
> are number of applications that have significant impact on our lives,
> and second is because it's really an intellectually, exciting and
> challenging field, which is one of the most interesting intellectual
> areas to pursue. I've listed here a number of applications. Perhaps
> the one that is most apparent to you is in movies. And all of you have
> perhaps seen Pixar's recent Brave film. A number of other movies are
> completely computer generated nowadays. 1995 Toy Story by Pixar was
> the first completely computer graphics movie. Today, almost every
> movie produced has significant computer graphics effects. 3D video
> games are again another popular area, and over the years we've seen
> their visual quality increased to the point that many times they are
> now close to movie quality in some ways. But one of the earliest
> applications of computer graphics was in computer aided design. Today
> if you consider a Boeing airplane, it's made completely on the
> computer, computer aided design. Different parts of it may be made in
> different continents and they come together, they work perfectly.
> Lighting simulation is one very important area in computer graphics
> and it's an aspect of realistic image synthesis. So, lighting
> simulation is important to create realistic simulations of how the
> interiors of buildings, interiors of rooms will look. How an
> automobile will look in an outdoor lighting environment. And computer
> graphics is used for all of these applications. It can be used for
> scientific visualization as well as medical visualization. We have the
> Visible Human Project. Many other projects where computer graphics is
> really critical for visualization. And of course in virtual reality
> systems where you combine the real with the virtual. And these have
> been critical since the very early days of computer graphics. Things
> like flight simulators and so forth. Of course, today we are
> surrounded by digital visual media, of which computer graphics is an
> integral part. And if you think about the types of visual media we've
> consumed, even on the internet, it's gone from text, to images, to
> video. And perhaps the next wave in media is 3D geometric models. And
> the real basics or real foundations of computer graphics. But of
> course even before that, computer graphics is essential to image and
> video processing and photography. Adobe was one of the first graphics
> companies that was started, and is really foundational to the way we
> handle images and video. Visual media are so prevalent. We have
> Flickr. YouTube. WebGL. All ways in which we can consume visual media
> online. And even the distinction between real and virtual worlds
> begins to blur with ideas like Google Earth, Second Life where you can
> have very realistic flythroughs of the real world. You can have
> completely virtual worlds in which actors and people actually work.
> Electronic publishing, online gaming is nowadays a huge market and is
> perhaps the biggest driver of games. And even going further, we are
> now seeing a vast revolution in 3D printers and fabrication, where we
> will be able to print real 3D objects, perhaps with realistic material
> properties. It's an area in which I am actually interested in
> research. Visual media are now a really prevalent part of our lives,
> and over the next 5 to 10 years, we can expect to see dramatic
> advances. Those are motivations in terms of the applications and the
> utility to our daily lives. But going well beyond that, computer
> graphics is also a field of interest because of its intellectual
> vitality. There are fundamental intellectual challenges. How do we
> create and interact with realistic virtual worlds? One of the goals in
> computer graphics is to simulate and build virtual worlds that behave
> much the way as the real worlds. How do we do this? And in creating a
> realistic virtual world you need to understand all aspects of the
> physical world. Beyond this we need to be able to understand new
> computing methods, new display technologies, we've seen great advances
> in all of these areas. And there are technical and intellectual
> challenges. How do we understand the mathematics required to do 3D
> computer graphics? How do I take an object and position it correctly
> on the screen? How do I draw surfaces that can be used in 3D computer
> graphics and will be starting the mathematics for all of these
> different aspects. How do I light an object correctly? How do I place
> the highlights of it properly? How do I place the smooth shading on it
> properly? This requires an understanding of the physics of lighting
> and shading. How are objects lit in the real world? And there are deep
> system challenges. How do we build 3D graphics programming software
> and hardware? And in fact, over the years, we have seen the 3D
> graphics hardware graphic processors have become useful even widely
> beyond the need of computer graphics. So, what we have seen here is
> that computer graphics has numerous applications and it involves
> fundamental intellectual and technical challenges which make it one of
> the most exciting areas to study and I hope you will join us in this
> course.


--

# L1V2: ONLINE GRAPHICS OVERVIEW: COURSE OUTLINE AND LOGISTICS

#### Unit 0 > Lecture 1: Course Overview > L1V2: ONLINE GRAPHICS OVERVIEW: COURSE OUTLINE AND LOGISTICS
 
## L1V2: Online Graphics Overview: Course Outline and Logistics

> Welcome back. In this segment we're going to go over some of the
> course logistics and give a brief overview of what the course is
> about. What the course outline is. First we introduce the notion of
> the 3D graphics pipeline. The graphics pipeline consists of 3 stages:
> modeling, animation and rendering. First let's talk about modeling.
> That is the process of creating geometric models of objects we're
> interested in. This could be a simple model of an object like a
> teapot. It could be a complicated mesh of an object like a cat
> sculpture. Or it could be a 2 billion polygon mesh of Michelangelo's
> David that was scanned several years ago by Professor Levoy and
> collaborators. The next step if you want the objects to actually move
> is to consider the animation or the motion of characters. And this is
> a rich area. We often want vibrant humanoid motion. In other cases we
> just want motion of objects from one place to another. The final step
> is rendering or creating realistic images, given the geometry and the
> animation. And there we want to simulate the way the light propagates
> in the scene to create effects like realistic and intricate shadow
> details, such as what you see in images on the right. In this course,
> we are going to have assignments that cover modeling and rendering
> parts of the graphics pipeline to give you basic understanding of
> computer graphics. In this course, we are not going to have time to go
> into animation in detail. We hope there will be a future course that
> deals with that. The first assignment deals with transformations and
> the goal there to place the objects in the world and view them. In
> particular, you will write a simple viewer that will view a teapot
> placed at the center of the screen and you will have to move around
> the teapot and create images in that way. The next 2 assignments deal
> more with rendering aspects of the course. So, in particular homework
> 2 is the scene viewer, and there you want to be able to view the scene
> the user specifies, and you want to be able to do it, with realistic
> lighting, with realistic materials, and as specified by the user. In
> homework 3, you will build a ray tracer which is an offline method to
> create very visually high quality visually realistic images by tracing
> rays that arise from the camera and go through each pixel in the
> image. I've said rasterize and I have said raytrace. Rasterization
> refers to your assignment in homework 2. So rasterization refers to
> homework 2, and raytracing refers to homework 3. These are
> fundamentally two different ways in which you can create images.
> Rasterization essentially goes through all the geometric primitives
> and dertermines where in the screen they should go. Raytracing does
> the opposite thing which goes to each point or each pixel in the
> screen and determines which geometric primitive that corresponds to.
> They each have their advantages and disadvantages, namely raytracing
> can produce higher quality images, but has historically been slower.
> We'll talk about the distinctions between them later in the course.
> But the nice thing is that homeworks 2 and 3 present ways in which you
> can create images of the same screen, same scene using both raytracing
> and rasterization. And this is the basic knowledge of computer
> graphics that this course seeks to give you. Let me talk a little bit
> about assignment logistics. The immediate task, you need to fulfill is
> to complete homework 0 and that enables you to ensure that you have
> the right kind of code compilation framework setup for all of the
> assignments. Now for all of the assignments including homework 0, we
> will have feedback and grading servers. And what that enable you to do
> is that you submit images that your program has produced. Our servers
> will compare these to the images that should have been produced and
> they'll return you a score and a difference image essentially noting
> what the differences are. Now you may wonder how you generate all the
> images that are needed. So the program's skeletons that we provide do
> most of that work automatically. For the raytracer you generate the
> images yourself. And you can submit the assignment multiple times. So
> you get feedback about what is working, what is not working. You can
> fix it and resubmit. Only your last submission will be counted. The
> skeleton code we provide in C++, Open GL, GLSL for Homework 0, 1 and 2
> enables you to focus on the parts that you really need for the
> assignment. At the same time, you do get a chance to write a raytracer
> from scratch, so that's a good experience to have. To progress in this
> course, you do need a good programming background, in C, C++ or Java.
> The language doesn't matter that much, but the programming in this
> course will be in C++. You do not need any prior knowledge of 3D
> graphics or of programming in open GL or GLSL. Let me say a little bit
> about the workload. This course is structured to have essentially the
> same workload as the local Berkeley courses and in fact we're using
> essentially the same assignments and the same grading mechanism. And
> so I have the slide which I use for the local course as well, and it's
> a course which is a lot of fun and very rewarding to create visual
> computer graphics imagery. But it does involve a significant amount of
> work. And there are, in particular, 3 programming projects in the
> online course, and all of those do require significant effort. The
> later ones especially. The course also involves understanding of
> mathematical and geometric concepts and we will have a final here
> which will be multiple choice where you will be tested on those.
> Prerequisites as I noted, you need a solid programming background and
> beside that you need some basic mathematical skills. So we will have a
> review of linear algebra in the next lecture. And the mathematical
> skills are not really more than what you would get from basic high
> school course. All of our assignments involve programming on the
> graphics processor using the GL shading language. An interesting point
> in the last 10 years is the development of GPU, the Graphics
> Programming Unit, which has made the graphics, 3D graphics
> programmable and has really enabled a revolution in 3D computer
> graphics. This course is modern and uses GPUs. So in homework 0, 1 and
> 2, you will be using GLSL with programmable shaders. Nowadays shaders
> are programmable and portable across all platforms, including on your
> phone for example. But you may need to set up your environment and
> compilation framework correspondingly.

--

# L1V3: ONLINE GRAPHICS OVERVIEW: HISTORY

#### Unit 0 > Lecture 1: Course Overview > L1V3: ONLINE GRAPHICS OVERVIEW: HISTORY

## L1V3: Online Graphics Overview: History


> In this segment we are going to give a brief history of computer
> graphics as part of our initial lecture on an overview and history.
> The term computer graphics itself was coined by William Fetter of
> Boeing in 1960. The first graphics systems were developed in the mid
> 1950s, the US Air Force SAGE radar systems, and they were based in the
> development at MIT. I strongly encourage you, if you have an
> opportunity, to look at the video on the history of computer graphics,
> which was released by SIGGRAPH for its 25th anniversary, which
> although somewhat dated, has an excellent introduction to the early
> part of the field. One of the interesting things I always like to do
> in this overview is to mention to people that text is in itself a
> major development in computer graphics. If you read Alan Turing's
> biography when he was developing the Manchester Mark I, he goes into a
> lot of details about the future potential of computers. Things like
> chess playing machines. Things like even compilers, to high level
> programming languages, but somehow even the notion of text escapes
> him. The Manchester Mark I, in its display essentially had a bank of
> LEDs. And so, you're just looking directly at the memory and trying to
> figure out what happens. So going from that, to our actual textual
> displays has been a major advance. And the way in which fonts are
> designed and the way in which they are displayed in the scene, on the
> screen in order to create a smooth appearance are some of the very
> interesting early problems in 2D computer graphics. Of course, textual
> representations haven't been the main way in which computers have been
> used for many decades. And the major advance has been the notion of
> the graphical user interface. The graphical user interface has an
> interesting history. It was invented at Xerox Palo Alto Research
> Center in the 1970's, around 1975. But Xerox did not actually benefit
> the most from the development of the graphical user interface. So it
> was first used in the Apple Macintosh, and subsequently, has become a
> standard for use of any computer, on any computers anywhere. Drawing
> was one of the early applications of computer graphics. Ivan
> Sutherland's Sketchpad system, which was developed to MIT in the
> 1960s, and was way ahead of its time. It introduced many of the
> concepts for drawing in current systems. Things like pop up menus,
> constraint based drawing, hierarchical modeling. I've included a link
> there for a video that shows Sutherland's Sketchpad system. I would
> very strongly encourage you to look at that after this lecture.
> Sketchpad can be considered the first interactive computer graphics
> system and in fact the first PHD thesis in computer graphics. And it
> really set the stage for what computer graphics could do. Following
> that, there was also a lot of interest in the development of paint
> systems. And the SuperPaint system, which was developed by Richard
> Shoup and Alvy Ray Smith, again, at Xerox's Palo Alto research center
> in the 1970s. I've taken these images from the excellent introduction
> on the website which I've noted here, which Richard Shoup has put
> together. And this SuperPaint system really presages modern software
> technologies, things like Adobe Photoshop. In fact, Adobe was one of
> the early start-ups in computer graphics, and nowadays of course, we
> don't think twice about applying general manipulations to images.
> Image processing has been a very significant aspect of what we see on
> the screen. We rarely see images that have not been processed in some
> way. So you can alter images by cropping, scaling, compositing them.
> You can even add or remove objects. Sports broadcasts for televisions
> combine 2D and 3D processing whether it's showing the world record
> line at the Olympics, or it's showing which swimmer is in each lane.
> And even showing different advertisements to different regions, all of
> these things are possible by smart image and video processing. That's
> been a quick tour of 2D computer graphics. And I've gone over it just
> to make a point that 2D is not something we typically study in a
> graphics course anymore, but has really revolutionized the world we
> live in. And you cannot really imagine a world today without 2D
> computer graphics. But most of this course is about three-dimensional
> computer graphics, and I just want to give you a brief history of
> modeling and rendering aspects of that. Geometric modeling is the
> process of creating 3D geometry, which can then be used in a computer
> graphics system. In the '70s and '80s, one of the major developments
> was the creation of spline curves and surfaces. And these were
> geometric methods that enabled the Utah Teapot, as it's known, to be
> created. And this was developed at the University of Utah. And was at
> that time a very interesting model because the teapot has lots of
> interesting geometry. It's not a genus 0 surface. It has a handle. It
> has a spout and all of this could be developed with spline models.
> More recently there's been a lot of interest in acquiring 3D geometry
> from the real world and representing it as triangle meshes that are
> acquired from real objects. And so I've shown you this simple 3D scan
> I did several years ago of this cat sculpture, and you can see the
> actual triangular 3D mesh elements there. Nowadays we've had scans of
> statues going into billions of polygons. A very famous effort is by
> Professor Levoy at Stanford and collaborators the Digital Michelangelo
> Project where there were scans of many of the statues of Michelangelo
> including a 2 billion polygon model of the David. And geometry is
> getting ever more complicated, and ever more interesting. Next we come
> to computer graphics rendering. And so in the 1960's the challenge was
> handling visibility. And there were a number of techniques which were
> proposed. So, this is hidden line algorithms, hidden surface
> algorithms. So, what I'm going to show you here is an image where I've
> just drawn all of the lines on the objects. And this leads to an
> interesting kind of image because you see there is no real notion of
> which object is in front of which object. For example this is the
> torus and if I look at it and I look at the cube or I look at the
> teapot and I look at the wall, you can see that the teapot should
> actually be blocking the wall but I can see the line of the wall
> through the teapot. So I have no real way of interpreting which object
> is in front of each other. That immediately leads to the problem of
> hidden line elimination. I want to eliminate the lines that I cannot
> see. And this is a challenge in art as well to create images that
> convey the notion of depth perception. So this was a problem in the
> 1960s, and Roberts and Appel worked on it, and came up with something
> that looks, now, a lot more interesting because you can actually
> perceive depth. You can say the cube is in front of the wall, the
> teapot is in front of the wall. Let me just do a comparison. So here
> it's very hard to even say which object is in front of which one,
> whereas here the hidden lines have been eliminated, and you have much
> better depth perception. And of course, hidden line elimination is one
> aspect of it, you can also extend it to hidden surface elimination.
> And so, this is addressing the fundamental challenge of visibility.
> Which object is before which object. Sutherland in 1974 wrote a famous
> paper that reduce visibility to sorting and compared a number of
> different visibility algorithms in this way. Of course once I've done
> this, I can also color the objects. But so far notice that they've
> just colored them in a constant color. And in particular, this image
> still looks, not so great. Look at this cone here. And what we see in
> this cone is you can clearly see the different facets of the different
> triangles which are being used to approximate the cone. Similarly, for
> this sphere you can see the polygonal outlines of the, of the
> triangles and the geometry that's being used to approximate the
> sphere. So this is not ideal yet. And therefore in the 1970s the
> challenge was, how can we get nice, smooth shaded image of this
> geometry. So I'm going to start with the image that I showed you
> earlier where you can clearly see the polygonal outlines. And, Henri
> Gouraud at the University of Utah in 1971 had a way to deal with these
> polygonal outlines and to interpolate the shading so that it would
> look smooth. So this is what is known as Gouraud shading. It's still
> used in OpenGL. You know it is smooth shading and suddenly the images
> look a lot smoother. And in fact they look like real curved surfaces.
> Not our computer graphics representations of them. However, they still
> looked like matte, or clay. And in fact they're just still a constant
> color. So the next innovation by Bui Tuong Phong was the notion of
> specular lighting, or Phong shading, and Phong illumination and Phong
> shading, models that still bear his name, are I would say still used
> in 99% of computer generated imagery. What Phong did was enable the
> use of highlights, which now makes it appear much more realistic. And
> in fact gives this plastic appearance where you have both a diffuse,
> or body color component and the specular highlight. Thereafter there's
> a lot of work. Jim Blinn and colleagues did substantial work on curved
> surfaces and texture. And in 1974 Ed Catmull introduced the notion of
> the z-buffer, or the hidden surface algorithm that is used nowadays in
> your graphics cards. Those challenges having been solved in the '80s
> and '90s, the next challenge was what was known as global
> illumination. Turner Whitted, in 1980, introduced the first recursive
> ray-tracing algorithm. It's what you will implement in homework 3, and
> you will, in fact, be able to produce images even better than this
> one. But transport yourself back to 1980 where you've just seen very
> simple computer graphic images, and some even have a bubble, which is
> refracting the surface, and you have reflections, refractions, all
> kinds of interesting visual effects. And this image from Turner
> Whitted is really canonical, and got many people excited about the
> prospect of computer graphics that it could really produce realistic
> imagery. The second revolution was in the area of radiosity, wherein
> you could simulate the interaction between the wall and one of the
> boxes. So in this case the small boxes, so here and here. They are
> actually made of neutral gray material. So all of the color is
> actually reflected from the wall. So the blue wall here reflects
> energy onto the box, and similarly the red wall here reflects energy
> onto the box. And in this way they had this reddish and bluish tinge.
> This is a famous image known as the Cornell Box. It's the Cornell Box
> and it was developed at Cornell University. Thereafter, Kajiya in 1986
> introduced something known as the rendering equation, which was a
> unified way to deal with many of the visual phenomena, such as the
> images on the left, from ray tracing or radiosity. And he produced
> this beautiful image, where all of the color again is coming from the
> caustics, from the green balls, the inter-reflections between the
> objects. And all of the objects, except for the green balls, are a
> neutral gray color. And in this way he had a number of visual effects
> that people found very hard to do in a unified framework. And, indeed,
> much of the 80's and 90's involved ways to solve the rendering
> equation. And this challenge to consider global illumination of light
> from everywhere in the scene, remains a challenge to the current day.
> Furthermore, our goal nowadays is to create photo-realistic images.
> That is, images that look just the way a real photograph would. And
> increasingly, the challenge is also to do it in real time. Real time
> photo-realism, and that is a frontier that now, for the first time, we
> are beginning to be able to reach. Finally I've talked about the
> history of modeling and rendering. Of course the history of computer
> animation and of computer graphics in general is also very crucially
> important. I would highly recommend this clip, I've given the URL
> below, which has an excellent 10 minute clip from the video on the
> history of computer animation. And it covers some of the topics we've
> discussed. So in particular, Sketchpad, animation, basic modeling and
> rendering. And really gives you a good synopsis of what 3D computer
> graphics and this course is about.


## Recommended videos

#### History of Computer Graphics (1972) - SIGGRAPH for its 25th anniversary
https://www.youtube.com/watch?v=NXkkr0REEPI

#### Sutherland's Sketchpad system
http://www.youtube.com/watch?v=mOZqRJzE8xg

#### Ivan Sutherland Sketchpad Demo
https://www.youtube.com/watch?v=6orsmFndx_o

#### history of computer animation
https://www.youtube.com/watch?v=LzZwiLUVaKg

--

