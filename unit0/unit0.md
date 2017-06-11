# Unit

### Welcome to CSE 167x

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


---

#### Unit 0 > Lecture 1: Course Overview > L1V1: ONLINE GRAPHICS OVERVIEW: MOTIVATION
# L1V1: ONLINE GRAPHICS OVERVIEW: MOTIVATION

### L1V1: Online Graphics Overview: Motivation

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


---

#### Unit 0 > Lecture 1: Course Overview > L1V2: ONLINE GRAPHICS OVERVIEW: COURSE OUTLINE AND LOGISTICS
# L1V2: ONLINE GRAPHICS OVERVIEW: COURSE OUTLINE AND LOGISTICS

### L1V2: Online Graphics Overview: Course Outline and Logistics

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

---

#### Unit 0 > Lecture 1: Course Overview > L1V3: ONLINE GRAPHICS OVERVIEW: HISTORY
# L1V3: ONLINE GRAPHICS OVERVIEW: HISTORY

### L1V3: Online Graphics Overview: History


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

---

### Recommended videos

#### History of Computer Graphics (1972) - SIGGRAPH for its 25th anniversary
https://www.youtube.com/watch?v=NXkkr0REEPI

#### Sutherland's Sketchpad system
http://www.youtube.com/watch?v=mOZqRJzE8xg

#### Ivan Sutherland Sketchpad Demo
https://www.youtube.com/watch?v=6orsmFndx_o

#### history of computer animation
https://www.youtube.com/watch?v=LzZwiLUVaKg

---



#### Unit 0 > Lecture 2: Basic Math > L2V1: BASIC MATH: VECTORS AND DOT PRODUCTS
# L2V1: BASIC MATH: VECTORS AND DOT PRODUCTS

### L2V1: Basic Math: Vectors and Dot Products


> Welcome to the second lecture of this online sequence. This is a
> review of the basic math you need for computer graphics and in
> particular, this first segment deals with vectors and dot products.
> Let me first say a few words about the next steps for the course.
> First, you should complete homework 0. And being able to compile
> homework 0 will ensure you have your compilation set up, OpenGL.
> Second, by actually submitting homework 0, you will ensure that you
> are able to use our feedback and grading servers properly, you are
> able to generate the images that they require. The first few lectures
> in this course talk about some of the core mathematical and technical
> ideas in computer graphics. They're some of the most beautiful ideas
> in computer graphics. Homework 1 has only a few lines of code, so it's
> relatively simple compared to homeworks 2 and 3. But I should mention
> that you should still start early on homework 1, because it is the
> first homework, and moreover, even though it only has a few lines of
> code, there is quite some thinking to be done. The idea of homework 1
> is to use some of the ideas in the first few lectures to generate your
> first images. As far as textbooks for the course, there is none
> required. This course is intended to be free and available to anyone.
> If you are, however, interested in getting a reference, then a
> reference for OpenGL and the GL shading language are useful. The
> standard red book for OpenGL, and the orange book for the GL shading
> language. But, I want to emphasize that there are no required
> textbooks and there's nothing that you need to purchase for this
> course. We start with the overall motivation of this section. Many
> computer graphics concepts need basic mathematics like linear algebra.
> We are interested in vectors, dot products, cross products. We are
> interested in matrices, matrix-vector and matrix-matrix
> multiplication. How does this come up? Assume for example that you
> have a point that you want to translate to a different region. This
> comes up all the time, you have a character, you want to move it
> somewhere else in the scene. You can regard the point as a vector and
> we'll see how an operation like translation, rotation can be written
> as a matrix-vector mulitiplication. The contents of this lecture on
> vectors and matrices should be very basic for most of you. It does not
> go beyond what you would learn in a basic high school mathematical
> education. We'll start by talking about vectors. Vectors are usually
> written with the vector symbol, so this is the common vector symbol,
> an arrow on top. Or, if you look at the textbook, they are often
> written in bold. The magnitude is written in the standard way by
> putting a norm symbol around the vector. Vectors have a length and
> they have a direction. The absolute position of a vector is not
> important. And so these 2 vectors are actually the same. So this
> vector moves here and I just translated the vector here, but they are
> actually the same vector. Vectors are used to store offsets,
> displacements and locations. But strictly speaking, there is a minor
> technical difference, that a position is not strictly speaking a
> vector and in fact you cannot add positions as vectors, because to
> have a positions such as 2 units on the X axis, we implicitly require
> an origin. Whereas, a vector is supposed to be independent of the
> origin, can be translated with respect to itself. Nevertheless, it is
> very convenient to also represent positions as vectors, and to
> multiply them as matrices to do various transformations. The first
> vector operation we are going to consider is vector addition. And so
> you have 2 vectors a and b, and you want to find what is the vector, a
> + b. This can be done geometrically with what is known as, the parallelogram rule. So, here you have the vector a. I take the vector
> b and I translate it, so that the tail of vector b is aligned with the
> head of vector a. And I complete the parallelogram and the diagonal of
> the parallelogram is the addition. If you don't want to think in terms
> of parallelograms, just think about it in terms of a triangle. So, I
> am considering the vector a + b from the tail of a to the head of b.
> Vector addition is commutative, so a + b is equal to b + a and if you
> are not very much into parallelograms, then we can consider it as
> simply adding coordinates in Cartesian components. So let's consider
> Cartesian coordinates, your familiar X and Y coordinates. I've shown
> the X axis and the Y axis. The vector I've shown here can be moved to
> the origin of the Cartesian coordinate system. And you can see in this
> case, it has 4 units along the X axis and 3 units along the Y axis. So
> the vector can be written as 4 times the unit X vector plus 3 times
> unit Y vector. X and Y, in this case are the coordinates of the axis.
> But, in general they can be any orthogonal unit vector. So, I write
> the vector A as the components X and Y. It's also interesting,
> sometimes, to write the transpose of A. So I'm writing a vector as a
> column vector. It transposes a row vector, x and y. And the norm of A
> is going to be square root of x^2 + y^2. Which, in this case, is the
> square root of 4^2 + 3^2 which will be equal to 5. That's just the
> Pythagorean relationship. It's important to note that x and y can be
> any unit vectors. Vectors can also be multiplied and in fact there are
> 2 multiplications of vector, the dot or the scalar product and the
> cross or the vector product. Note that in this lecture we will use
> right-handed coordinates, which is a standard coordinate system found
> in most mathematics textbooks. What do right-handed coordinates mean?
> If you take your right hand and your X axis is pointed here, your Y
> axis is pointed here. If you take your hand and you curl them around
> the X and Y axes, the thumb on the right hand will point towards the
> positive Z axis. With left-handed coordinates it would of course be
> the opposite and so we assume right-handed coordinate system with
> obvious due apologies to those of you who are left-handed. First,
> let's consider the dot or the scalar product and that is written as a
> dot b. It's commutative. It's also equal to b dot a. We want to
> consider the norm of a, so of course the product involves the product
> of the two vectors a and b, so we do want to consider this norm of a.
> And now of course it is symmetric, so we will also want to consider
> the norm of vector b. How does it depend on the angle between a and b?
> That's the crucial question. And its intended to be the product of
> their magnitudes when the vectors are aligned. But, when they are not
> aligned, we will have to multiply it, by the cosine of the angle
> between them. My handwriting is not the best and throughout this
> course when you need an actual equation, I will put it on the slide as
> well. As we see here, a dot b is the norm of a times norm of b times
> the cosine of the angle between them. From that equation, you can
> calculate the angle between two vectors, as the inverse cosine of a
> dot b divided by each of their individual magnitudes. This is in fact
> is one of the most common uses of the dot product, because the dot
> product can be calculated very efficiently in Cartesian components,
> but the angle between two vectors not that easily. So, what you do is,
> you take the dot product, and then by taking the inverse cosine, you
> get the angle between the 2 vectors. The dot or scalar products has
> the associativity and the multiplication properties. So a dot (b + c)
> is equal to a dot b + a dot c. And if you multiply a scalar through
> any of the vectors k dot b or uh, a dot kb that just multiplies the
> dot product by a scalar. The question now is, what is the dot product
> in Cartesian components? And this is something we can derive. So I
> write the dot product as x_a. And now, this is in a particular
> direction. So it's in the direction of the X vector. And the next
> coordinate is y_a, which is in the direction of the Y vector. Okay, so
> I am going to take dot product of this with the same thing for b and b
> will be written as x_b times the X vector plus y_b times the Y vector.
> If we now consider and expand these things out, we have the following.
> So we have x_a
> * X times x_b * X and I can write that. I can also include the y_a * y_b term and that will multiply Y dot Y. Finally, I can include the X
> dot Y terms. X dot Y terms and so I can write plus X dot Y. And that
> will be multiplied by x_a * y_b + x_b * y_a. But what you can
> immediately realize is that, because the cosine of the angle between X
> and Y is 0, the angles X and Y are away by 90 degrees. Cosine of 90
> degrees is 0. So this quantity is actually equal to 0. And therefore,
> we only care about this term here. And, of course, if you could not
> quite follow my handwriting, I, again, have the equation on the next
> slide. Where a dot b is equal to the dot product of [x_a, y_a] and
> [x_b, y_b]. And this is simply equal to x_a * x_b plus y_a * y_b. Very
> Simple. Let's look at some applications in computer graphics. The
> obvious one is to find the angle between two vectors, I already talked
> about it. The cosine of the angle between the light source and the
> surface is very important for shading. It's also important to find the
> projection of one vector on another. Example, if we want a
> co-ordinates of a point in new co-ordinate system. And the advantage
> of the dot product is that it is easily computed in Cartesian
> coordinates. So let's now as a final step look at the projection of
> vector b on a. So very often you want to know what fraction of the
> vector b lies on a. And this can be done easily with the dot product.
> Essentially it's equal to the norm of the vector b, times the cosine.
> So we can say that the projection of the vector b on a is equal to the
> norm of the vector b times the cosine of the angle between them.
> Because that's the definition, the component of b along vector a is
> given by the cosine. And this is simply a dot product of the vector a
> and the vector b, which is what the cosine is, divided by the norm of
> a and the norm of b. Now the norm of b cancels and what you are left
> with is the dot product of a and b divided by the magnitude of the
> vector a. And so the question is what is the component of b along a
> given by? We will have to multiply by the unit vector along the a
> direction. We already have the length in the first formula but now you
> need to multiply by this term. So this term here is the unit vector.
> So it is the unit vector which has a length of 1. And you multiply by
> that. Now, b projection on a is a dot b / norm of a, multiplying by
> the vector a, and dividing by norm of a, makes norm of a squared. And
> so what you are left with, is the projection of b on the vector a, is
> this quantity, which involves the dot product between a and b. And the
> projection is of course, along the direction of the vector a, which is
> why the final result involves the vector a.


### Key concepts

*  Dot (scalar) product 

*  Dot product: some applications in CG
  1. Find angle between two vectors (e.g. cosine of angle between light source and surface for shading)
  2. Finding projection of one vector on another (e.g. coordinates of point in arbitrary coordinate system)
  3. Advantage: computed easily in cartesian components

### Reference

*  The standard red book for OpenGL
*  The orange book for the GL shading language

---



#### Unit 0 > Lecture 2: Basic Math > L2V2: BASIC MATH: CROSS PRODUCTS
# L2V2: BASIC MATH: CROSS PRODUCTS

### L2V2: Basic Math: Cross Products


> Welcome to the second lecture of this online sequence. This is a
> review of the basic math you need for computer graphics and in
> particular, this first segment deals with vectors and dot products.
> Let me first say a few words about the next steps for the course.
> First, you should complete homework 0. And being able to compile
> homework 0 will ensure you have your compilation set up, OpenGL.
> Second, by actually submitting homework 0, you will ensure that you
> are able to use our feedback and grading servers properly, you are
> able to generate the images that they require. The first few lectures
> in this course talk about some of the core mathematical and technical
> ideas in computer graphics. They're some of the most beautiful ideas
> in computer graphics. Homework 1 has only a few lines of code, so it's
> relatively simple compared to homeworks 2 and 3. But I should mention
> that you should still start early on homework 1, because it is the
> first homework, and moreover, even though it only has a few lines of
> code, there is quite some thinking to be done. The idea of homework 1
> is to use some of the ideas in the first few lectures to generate your
> first images. As far as textbooks for the course, there is none
> required. This course is intended to be free and available to anyone.
> If you are, however, interested in getting a reference, then a
> reference for OpenGL and the GL shading language are useful. The
> standard red book for OpenGL, and the orange book for the GL shading
> language. But, I want to emphasize that there are no required
> textbooks and there's nothing that you need to purchase for this
> course. We start with the overall motivation of this section. Many
> computer graphics concepts need basic mathematics like linear algebra.
> We are interested in vectors, dot products, cross products. We are
> interested in matrices, matrix-vector and matrix-matrix
> multiplication. How does this come up? Assume for example that you
> have a point that you want to translate to a different region. This
> comes up all the time, you have a character, you want to move it
> somewhere else in the scene. You can regard the point as a vector and
> we'll see how an operation like translation, rotation can be written
> as a matrix-vector mulitiplication. The contents of this lecture on
> vectors and matrices should be very basic for most of you. It does not
> go beyond what you would learn in a basic high school mathematical
> education. We'll start by talking about vectors. Vectors are usually
> written with the vector symbol, so this is the common vector symbol,
> an arrow on top. Or, if you look at the textbook, they are often
> written in bold. The magnitude is written in the standard way by
> putting a norm symbol around the vector. Vectors have a length and
> they have a direction. The absolute position of a vector is not
> important. And so these 2 vectors are actually the same. So this
> vector moves here and I just translated the vector here, but they are
> actually the same vector. Vectors are used to store offsets,
> displacements and locations. But strictly speaking, there is a minor
> technical difference, that a position is not strictly speaking a
> vector and in fact you cannot add positions as vectors, because to
> have a positions such as 2 units on the X axis, we implicitly require
> an origin. Whereas, a vector is supposed to be independent of the
> origin, can be translated with respect to itself. Nevertheless, it is
> very convenient to also represent positions as vectors, and to
> multiply them as matrices to do various transformations. The first
> vector operation we are going to consider is vector addition. And so
> you have 2 vectors a and b, and you want to find what is the vector, a
> + b. This can be done geometrically with what is known as, the parallelogram rule. So, here you have the vector a. I take the vector
> b and I translate it, so that the tail of vector b is aligned with the
> head of vector a. And I complete the parallelogram and the diagonal of
> the parallelogram is the addition. If you don't want to think in terms
> of parallelograms, just think about it in terms of a triangle. So, I
> am considering the vector a + b from the tail of a to the head of b.
> Vector addition is commutative, so a + b is equal to b + a and if you
> are not very much into parallelograms, then we can consider it as
> simply adding coordinates in Cartesian components. So let's consider
> Cartesian coordinates, your familiar X and Y coordinates. I've shown
> the X axis and the Y axis. The vector I've shown here can be moved to
> the origin of the Cartesian coordinate system. And you can see in this
> case, it has 4 units along the X axis and 3 units along the Y axis. So
> the vector can be written as 4 times the unit X vector plus 3 times
> unit Y vector. X and Y, in this case are the coordinates of the axis.
> But, in general they can be any orthogonal unit vector. So, I write
> the vector A as the components X and Y. It's also interesting,
> sometimes, to write the transpose of A. So I'm writing a vector as a
> column vector. It transposes a row vector, x and y. And the norm of A
> is going to be square root of x^2 + y^2. Which, in this case, is the
> square root of 4^2 + 3^2 which will be equal to 5. That's just the
> Pythagorean relationship. It's important to note that x and y can be
> any unit vectors. Vectors can also be multiplied and in fact there are
> 2 multiplications of vector, the dot or the scalar product and the
> cross or the vector product. Note that in this lecture we will use
> right-handed coordinates, which is a standard coordinate system found
> in most mathematics textbooks. What do right-handed coordinates mean?
> If you take your right hand and your X axis is pointed here, your Y
> axis is pointed here. If you take your hand and you curl them around
> the X and Y axes, the thumb on the right hand will point towards the
> positive Z axis. With left-handed coordinates it would of course be
> the opposite and so we assume right-handed coordinate system with
> obvious due apologies to those of you who are left-handed. First,
> let's consider the dot or the scalar product and that is written as a
> dot b. It's commutative. It's also equal to b dot a. We want to
> consider the norm of a, so of course the product involves the product
> of the two vectors a and b, so we do want to consider this norm of a.
> And now of course it is symmetric, so we will also want to consider
> the norm of vector b. How does it depend on the angle between a and b?
> That's the crucial question. And its intended to be the product of
> their magnitudes when the vectors are aligned. But, when they are not
> aligned, we will have to multiply it, by the cosine of the angle
> between them. My handwriting is not the best and throughout this
> course when you need an actual equation, I will put it on the slide as
> well. As we see here, a dot b is the norm of a times norm of b times
> the cosine of the angle between them. From that equation, you can
> calculate the angle between two vectors, as the inverse cosine of a
> dot b divided by each of their individual magnitudes. This is in fact
> is one of the most common uses of the dot product, because the dot
> product can be calculated very efficiently in Cartesian components,
> but the angle between two vectors not that easily. So, what you do is,
> you take the dot product, and then by taking the inverse cosine, you
> get the angle between the 2 vectors. The dot or scalar products has
> the associativity and the multiplication properties. So a dot (b + c)
> is equal to a dot b + a dot c. And if you multiply a scalar through
> any of the vectors k dot b or uh, a dot kb that just multiplies the
> dot product by a scalar. The question now is, what is the dot product
> in Cartesian components? And this is something we can derive. So I
> write the dot product as x_a. And now, this is in a particular
> direction. So it's in the direction of the X vector. And the next
> coordinate is y_a, which is in the direction of the Y vector. Okay, so
> I am going to take dot product of this with the same thing for b and b
> will be written as x_b times the X vector plus y_b times the Y vector.
> If we now consider and expand these things out, we have the following.
> So we have x_a
> * X times x_b * X and I can write that. I can also include the y_a * y_b term and that will multiply Y dot Y. Finally, I can include the X
> dot Y terms. X dot Y terms and so I can write plus X dot Y. And that
> will be multiplied by x_a * y_b + x_b * y_a. But what you can
> immediately realize is that, because the cosine of the angle between X
> and Y is 0, the angles X and Y are away by 90 degrees. Cosine of 90
> degrees is 0. So this quantity is actually equal to 0. And therefore,
> we only care about this term here. And, of course, if you could not
> quite follow my handwriting, I, again, have the equation on the next
> slide. Where a dot b is equal to the dot product of [x_a, y_a] and
> [x_b, y_b]. And this is simply equal to x_a * x_b plus y_a * y_b. Very
> Simple. Let's look at some applications in computer graphics. The
> obvious one is to find the angle between two vectors, I already talked
> about it. The cosine of the angle between the light source and the
> surface is very important for shading. It's also important to find the
> projection of one vector on another. Example, if we want a
> co-ordinates of a point in new co-ordinate system. And the advantage
> of the dot product is that it is easily computed in Cartesian
> coordinates. So let's now as a final step look at the projection of
> vector b on a. So very often you want to know what fraction of the
> vector b lies on a. And this can be done easily with the dot product.
> Essentially it's equal to the norm of the vector b, times the cosine.
> So we can say that the projection of the vector b on a is equal to the
> norm of the vector b times the cosine of the angle between them.
> Because that's the definition, the component of b along vector a is
> given by the cosine. And this is simply a dot product of the vector a
> and the vector b, which is what the cosine is, divided by the norm of
> a and the norm of b. Now the norm of b cancels and what you are left
> with is the dot product of a and b divided by the magnitude of the
> vector a. And so the question is what is the component of b along a
> given by? We will have to multiply by the unit vector along the a
> direction. We already have the length in the first formula but now you
> need to multiply by this term. So this term here is the unit vector.
> So it is the unit vector which has a length of 1. And you multiply by
> that. Now, b projection on a is a dot b / norm of a, multiplying by
> the vector a, and dividing by norm of a, makes norm of a squared. And
> so what you are left with, is the projection of b on the vector a, is
> this quantity, which involves the dot product between a and b. And the
> projection is of course, along the direction of the vector a, which is
> why the final result involves the vector a.

### Key concepts

*  Cross (vector) product
*  Cross product: Cartesian formula?
*  Dual matrix of vector a 


---



#### Unit 0 > Lecture 2: Basic Math > L2V3: BASIC MATH: CREATING A COORDINATE FRAME
# L2V3: BASIC MATH: CREATING A COORDINATE FRAME

### L2V3: Basic Math: Creating a Coordinate Frame


> Welcome. In this segment, we are going to see how to use dot and cross
> products to create an orthonormal coordinate frame which will be
> useful in many applications. Orthonormal bases and coordinate frames
> are important for representing points, positions, locations. Often
> there are many different sets of coordinate systems. So not just your
> single XYZ coordinate systems. In graphics this is very common that
> you will have a coordinate system associated with the model, you will
> have a coordinate system associated with the local coordinates, you
> will have a coordinate system associated with the world, you may even
> have separate coordinate systems for the head, for the shoulder, for
> the hands, for the torso, for the legs, for the shoes, so on. And a
> very important part is to get all of these different objects in their
> consistent frame of reference. So a critical issue is transforming
> between these different coordinate systems. In fact the next 3
> lectures deal with the transformations and viewing and the way in
> which you can use matrices and vectors for that purpose. So what is a
> coordinate frame? It's any set of 3 vectors in 3 dimensions, such that
> the vectors are of unit norm. Such that the vectors are mutually
> orthogonal to each other. And such that they obey this cross product
> relationship, which is that w is equal to u cross v. You can think of
> all of these in terms of X, Y and Z. Of course, the unit X, Y and Z
> vectors are of unit norm. Of course they're mutually orhtogonal with
> respect to each other. And, of course, the Z vector is simply equal to
> X cross Y. One of the interesting things about this is that a vector p
> can be written in terms of its projections onto the vectors u, v and
> w. So, p dot u is the projection onto the vector u, with the vector u.
> p dot v is the projection onto the vector v, times the vector v. p dot
> w is the projection onto the vector w, times the vector w. How do you
> construct the coordinate frame? So, the first question, why do you
> want to construct the coordinate frame? It's often the case that
> you're given a vector a, which in homework 1, will be the viewing
> direction. You want to create an orthonormal basis from this. But of
> course, an orthonormal basis involves 3 unit vectors and you can't get
> it from a single vector, so need a second vector b, which in homework
> 1 is the up direction of the camera. So given 2 vectors a and b, how
> to you create an orthonormal coordinate frame? Intuitively, you want
> to associate the vector w with a and the vector v with b. But, a and b
> are neither orthogonal vectors nor are they a unit norm, and we also
> need to find the u vector. First let's try to find what the vector w
> is equal to. And the vector w should just be given by the vector a in
> this case. But the only problem with this is that A is not of unit
> norm, so we need to normalize it. And we simply divide by the
> magnitude of the vector a. So that part is simple, the vector w is
> equal to the a divided by the unit norm of a. But how do we get v and
> u? That part is complicated, so why is is complicated? If the vector b
> is orthogonal to the vector a you're completely fine, you can just
> define b based on that. The vector b may not be orthogonal to the
> vector a. So one thing to do is to remove its projection in the
> direction of a which would be a dot product but there is in fact a
> more elegant way of doing this. Even though b and now w are not
> necessarily orthogonal to each other we can use the cross product to
> find the third vector which is orthogonal to both b and w. So instead
> of finding the vector v, we first find the vector u. You write the
> vector u as equal to b cross product with w and divide the whole thing
> by the norm of b cross w. And that's the formula I have written here,
> u is equal to b cross w divided by the norm of b cross w. The final
> step we need here, is to find the vector v, but given w and u, v is
> given by, w cross product with u. In this way you have created a
> complete coordinate frame, given 2 vectors, that need not be unit
> norm, that need not be orthogonal. Of-course this fails when the norm,
> when this quantity is equal to zero, so if b and w are aligned with
> each other, in which case their cross product is equal to zero, then
> they are really the same vector, a and b are the same vector and you
> cannot create the coordinate frame.


---



#### Unit 0 > Lecture 2: Basic Math > L2V4: BASIC MATH: MATRICES

# L2V4: BASIC MATH: MATRICES


### L2V4: Basic Math: Matrices


> In the previous segments, we have studied various aspects of vectors.
> In this segment, we will talk about matrices, which are also very
> important. Most transformations involve a matrix multiplying a vector.
> Matrices can be used to transform points. The next few lectures will
> talk about their use for translation, rotation, shears, scales. In
> fact, all transformations and the graphics pipeline are handled by
> matrices. First question, what is a matrix. Its just an array of
> numbers. It has m rows, in this case 3 rows, and n columns, in this
> case 2 columns. Operations you can do on a matrix. Addition and
> multiplication by a scalar are simple. They're just applied to each
> element of the matrix. So if you add one matrix to another matrix you
> just do element by element addition. If you want to multiply a matrix
> by scalar you just scale up all the elements by a constant, by the
> scalar. The most interesting thing is matrix-vector and matrix-matrix
> multiplication. Note that a vector is a special case of a matrix. In
> our case, we have been using column vectors, so they have n rows and 1
> column. For matrix-matrix multiplication, the rules are that the
> number of columns in the first matrix, in this case the first matrix
> has 2 columns, must equal to number of rows, in this case 2 rows, in
> the second matrix. So if you multiply matrix m by n times another
> matrix n by k, the result will be m times k. Another way of thinking
> about this is that the element (i,j) in the product is a dot product
> of row i in the first matrix, and column j of the second matrix. So
> the condition that the number of columns in the first is equal to the
> number of rows in the second is simply a condition that we must be
> able to take dot products, the vectors must be of the same length. So
> here, I've shown how the matrix multiplication works. The highlight is
> on the first row of the first matrix and the result. Note that in
> element (i,j), so this is the element in the top left, and starting to
> number my rows and columns from 1, I can say that this is element
> (1,1). So it will be a dot product of row 1 and so I can number these
> rows as 1, 2, 3, and I can similarly number the columns as 1, 2, 3, 4.
> So it will be a dot product of row 1 and column 1 in order to
> highlight the different columns here I have used the color red. Ans so
> 1 times 3 is 3, 3 times 2 is 6, you add these together in the dot
> product. It's 9, and that's the value. Notice the color of
> highlighting so, red is used to highlight the first column here, first
> column here and so you get the dot product of [1, 3] and [3, 2] for
> this number. Similarly, for this number here its dot product of [1, 3]
> and [6, 7] so, 1 times 6 is 6, 3 times 7 is 21, you get 27. Now the
> next one, 1 times 9 is 9, 3 times 8 is 24, you get 33. 1 times 4 is 3
> times 3 is 9, you get 13. And similarly, we can apply this to the next
> row. And so we take the dot product with each column to give each
> element of this matrix. For example, for the first one, 5 times 3 is
> 15, 2 times 2 is 4, 19. 5 times 6 is 30, 2 times 7 is 14, 44. 5 times
> 9 is 45, 2 times 8 is 16, 61. 5 times 4 is 20, 2 times 3 is 6, 26. And
> the final example here, the first one is 0, so we don't even need to
> consider it. 4 times 2 is 8, 4 times 7 is 28, 4 times 8 is 32, 4 times
> 3 is 12. And this is the way matrix multiplication works. Matrix
> multiplication is not commutative. If I reverse the order of the
> matrices here, it's not even a legal operation. The number of columns
> in the first matrix, in this case, is 4. The number of rows in the
> second, in this case, is 3, and it's not commutative. Even if the
> matrices actually have dimensions that they can be multiplied, it's
> still not commutative. However, matrix multiplication is associative
> and distributive. So a * (b+c) is equal to ab + ac. (a + b) * c is
> equal to ac + bc. Matrix-vector multiplication is key for transforming
> the points and this is the main topic we will be treating in the next
> few lectures. We can treat the vector as a column matrix, m rows times
> 1 column. And just as a simple example, I've shown you 2D reflection
> about the Y axis, so let's talk about reflection for a minute. So I
> have my screen, this is the X axis, this is the Y axis, and I have a
> point here, which has some coordinates (x,y). I wish to reflect it
> about the Y axis to get a point here. And this will have coordinates,
> (-x,y). That's what reflection about the y axis is. If you think about
> this matrix equation, the new x coordinate is -1 times x plus 0 times
> y, which is -x, and 0 times x plus 1 times y, which is y. So
> reflection is given by this equation, [-1 0, 0 1], whereas the
> identity would just have this as plus 1. So this is a simple example
> of how matrix vector multiplication can be used to transform points
> corresponding to a particular operation. The other interesting thing
> we consider is the transpose of a matrix. And that simply replaces the
> rows with columns, so you can think of [1 2] being the first row
> becomes the first column, [3 4] second column, [5 6] third column. We
> can also transpose a vector in which the column vector becomes a row
> vector and vice versa. One interesting property on the matrix
> transpose, it also applies to matrix inverses, is that, if you want to
> transpose the product of 2 matrices, A and B, A times B transpose, you
> just transpose the individual matrices, so you transpose B and you
> transpose A, but you have to flip the order. So you have to reverse
> the order in which the transposes are applied. So it will be B
> transpose times A transpose. That's a very useful property to know.
> The identity matrix is useful to define, and so the dimensions of the
> matrix have noted here 3 by 3. It just has ones along its main
> diagonal, zeroes elsewhere. And the properties of the identity matrix
> is the matrix times its inverse is equal to inverse times matrix, is
> the identity. How do you, do the inverse of A times B, it's A inverse
> B inverse, but you have to change the order. So if I consider, B
> inverse times A inverse, times A, times B. You can see that this
> becomes the identity, and then B inverse times B, also becomes the
> identity. So changing the order is in fact, the right thing to do. If
> I don't change the order, the result is not the identity. Finally
> let's relate matrices back to the dot product and the cross product.
> And we want these vector multiplication operations, a dot b and a
> cross b to be represented in terms of matrix-vector multiplication. So
> a dot b just multiplies the same components of vector a with vector b,
> and there is a very easy way to represent this in matrices, as a
> transpose b (a^T * b). So, if the vector is a column vector, the
> transpose is x_a, y_a, z_a. The number of columns 3 is equal to the
> number of rows, and the dimensions of the matrix is the number of
> rows, here 1 and the number of columns, here 1. And so you have x_a *
> x_b + y_a * y_b + z_a * z_b. Next, we come to the cross product. We've
> already seen it when we discussed cross products. You can do it using
> the dual matrix of the vector a, and so you can represent it as "A
> star" (A*) times b, where A* is the dual matrix of the vector a.



### Key concepts

*  Matrices
*  Matrix-matrix multiplication
*  Matrix-Vector Multiplication
*  Transpose of a Matrix (or vector?)
*  Identity Matrix and Inverses
*  Vector multiplication in Matrix form


---


#### Unit 0 > Homework 0 > HOMEWORK 0: COMPILATION
# HOMEWORK 0: COMPILATION

### Introduction

This assignment gets all the groundwork ready so you can focus on the content in CSE 167x. In particular, you will make sure you know how to compile and run OpenGL programs with shaders.  Please read the entire assignment (there are multiple pages), including the FAQ on the last tab. 

### Compiling OpenGL Programs

Homeworks 1 and 2 in the class will be using OpenGL programs, including the use of modern programmable vertex and fragment shaders with the OpenGL shading language GLSL.

In principle, OpenGL and related code should be portable across many platforms, and indeed this is its strength. (In both our local classes and previous EdX classes, while there were niggling issues, almost nobody had difficulty getting a working setup, across a wide range of machines, operating systems, and coding frameworks). As such, you may use any computer and platform you choose, but will need some kind of C++ development framework and an installation of OpenGL and GLUT (more on these next).  

In practice, the above statement is pretty close to true, but you need different installs and tricks to get your machine set up to run the programs for this class properly; this differs on different operating systems. Moreover, the shading language is constantly evolving. Fortunately, we have a detailed FAQ for a variety of different systems.  If you come up with some interesting tricks to get things to work, please post on the discussion boards. As a practical matter, you cannot progress further in the course without being able to compile OpenGL and GLSL programs, and use our autograders, so treat this assignment as being of utmost importance.

The skeleton code for the assignments includes the GLM library which is available at http://glm.g-truc.net. This library is header-only, so should be very portable and includes many useful matrix-vector operations, and replacements for many deprecated functions. We have included the zip file and unpacked versions already in the skeletons, and modified include paths appropriately, so you should not need to download anything for GLM.


---

#### Unit 0 > Homework 0 > HOMEWORK 0: ASSIGNMENT

# HOMEWORK 0: ASSIGNMENT

Homework 0: Assignment

To make sure you can run programs for the course, please download and compile the homework 0 framework, that can be found from our our syllabus page, and reproduced below. Some of you may also wish to browse the lectures in Unit 2 which explain OpenGL and gradually build up the program used for homework 0. (However, Unit 2 is by no means required for homework 0, which just involves setup and compilation).

Homework 0 Framework

* Windows VS 2012 or later 
* Windows VS 2010
* OS X  (OS X: 10.9.x or later)
* OS X/Linux (OS X: 10.8.x [Mountain Lion] or earlier; Linux)

We include complete skeletons for major platforms. (In some cases, our versions include the compiled objectives and executable to help you, but please try to recompile the source code from scratch to make sure everything works.) If you develop on a different platform, you may need to re-create projects and Makefiles from the source code. The next page is a FAQ detailing compilation options.

The Homework 0 program has a textured ground plane with 4 "pillars" and a teapot with lighting that moves.

On Windows, you can run the program by opening the .sln file and pressing F5. On Mac OSX or Linux, you should use the command line to cd to the directory containing the files, type make and ./mytest3.   (Please do not double click on the file using finder in MacOS; that will lead to errors, since the paths would not be set up properly.  Similarly in Windows, please use your C++ development environment for running, by pressing F5 as noted above, rather than double-clicking the executable).  Please also note that the correct way to exit is to hit the ESC key in the program.

Note for this program, the shader directories that contain glsl shaders. These are files that are loaded and compiled by the OpenGL program at runtime and therefore must exist, but need not be part of the Makefile or project.

The mouse can be used to zoom in. Look at the keyboard function in mytest3.cpp to see the keys you can press. The p key will start and stop the animation of the teapot.

Once you have the program running successfully, press i to move the teapot into the correct position for our autograder. Next, press o to output the screenshot to the program's directory. Rename it to "screenshot1.png" so it isn't overwritten by a subsequent screenshot.   Please make sure you do not zoom in or out prior to pressing i or o (if you have earlier played with the mouse, it is best to restart the program and  take the screenshot).   

Next, I want you to change the color of the red highlight on the teapot to yellow (yellow is made by mixing red and green, which are the first two elements of the color vector: the third is blue). This corresponds to a RGBA value of (1,1,0,1). The relevant colors and code are defined in the "display" function of "mytest3.cpp" where it says "add lighting effects." Note that the red highlight is originally somewhat orange with a RGBA value of (1,0.5,0,1). Once you have changed the color of the highlight from red to yellow, recompile, run, and press i then o as before to output a screenshot. Rename this screenshot to "screenshot2.png".

#### Future Homework Frameworks

It is a good idea to visit the course syllabus and attempt to compile the later homework frameworks, so that we can catch any compilation issues early.

---

#### Unit 0 > Homework 0 > HOMEWORK 0: FAQ/COMPILATION NOTES

# HOMEWORK 0: FAQ/COMPILATION NOTES

### Homework 0: FAQ/Compilation Notes

The skeleton code already includes most needed dependencies, and will compile without problems in the vast majority of cases. So, most of you will not need to read this FAQ at all.   Also, as a first step, if you are having difficulties, please update the drivers for your graphics card.  (It's amazing how many issues were fixed by this simple operation in previous EdX classes).  As a general guideline, we do require support of OpenGL 2.1 and GLSL 120.  While almost any machine purchased in the last 5-6 years will support this, some integrated Intel graphics cards might not.  The only way to really test is to make sure homework 0 works.  In particular, if you get a message (on Windows) like exception at 0x00000000 in hw0-windows.exe: 0xC0000005: Access violation it may indicate an issue with your graphics card, and you need to upgrade drivers and/or try a different card/machine.

Please note that different computer systems produce slightly different images. We have set our thresholds in the autograder accordingly. Don't worry about a few pixels being off, as long as you pass the test.  Please also note that the autograder includes a visual watermark on the solution images, which will make them look slightly different from your own images, but will not affect the grading.  

Similarly, please ignore compiler warnings, as long as the program compiles and runs.  In particular, to allow for execution on the widest variety of older systems, we do use many backwards-compatible deprecated programming constructs, which may lead to a number of warnings on newer machines.  The programs will still compile and run, and if they do so, you may safely ignore these warnings.

If you still have difficulties passing the test and know your images are correct, please (1) Check the images are not zoomed (scaled) or resized in any way.  Also, please do not zoom into/maximize/etc the image before you press 'o' to take the final screenshots. (2) Turn off all antialiasing features for your graphics card; you may also need to set 3D anti-aliasing to Application Managed.  For Intel graphics cards, open the Intel HD Graphics Panel, go to 3D, set "Application Optimal Mode" to off.

Windows

Visual Studio Community 2017 edition (free for students, open source developers and individual developers) should be available for free at http://www.microsoft.com/visualstudio/eng/downloads which also may have links to older downloads (we support Visual Studio 2012 and later).  Please note that with VS 2015 and later, you must explicitly select C++ support when installing; by default only C# etc. is installed.  Failing to include C++ support will lead to lots of issues with missing headers etc.  If this does not work for you for whatever reason, we assume you can obtain Visual Studio or an equivalent C++ development environment by other means.  In the past, we've found another useful link as https://www.dreamspark.com/ where one can download Visual studio (2012, 2013, 2015+); however, that link may require being enrolled as a student in a regular academic program and providing academic verification.

Choose the right version for your computer. Please note that the Visual Studio Express 2012 (or 2013 or later) edition should be adequate for this course, and is free for everyone.  Some students have mentioned that it is necessary to use Visual Studio Express 2012 (or 2013) for Windows Desktop rather than just VS 2012 (2013/later) express for Windows.  The current version is Visual Studio Community 2017 (the instructions below for VS 2015 should still apply).  If you install this version of VS 2015 (or 2017), please ensure that you select the "Common Tools for Visual C++ 2015 (2017)" feature under "Programming Languages"/"Visual C++". If the above step isn't done correctly, the skeleton code may not be upgraded properly. If you installed Visual Studio 2015 or 2017 without this feature, you can re-run the installation program and modify Visual Studio to add the feature.  Please note that by default, VS 2015 does not include C++ support.  You must explicitly select C++ support in the installer when installing Visual Studio 2015.  (Otherwise only C# is supported, and you will get a bunch of errors with missing header files when compiling).

(Please note that we use a VS 2012 skeleton for backwards compatibility.  If you are using VS 2013 or VS 2015/2017, the skeleton will still work; you only need to click OK in the conversion/upgrade dialog once you open the skeleton code.  Similarly, if you are running on Windows 10, it may warn that the skeleton is configured for Windows SDK 8.1.  Please follow the instructions to retarget the solution.)  

If you are having issues taking screenshots, you can either manually crop a print screen (printscreen button) or use Fraps to take a screenshot (the manual method may be harder for later assignments however). Some students have reported that this issue can be fixed simply by changing the code to save the back buffer instead of the front (this is in the third line of the saveScreenshot() procedure in mytest3.cpp), that is by using

glReadBuffer(GL_BACK);
(Only) if you run into issues with 32/64-bit compilation, make sure your platform target says Win32, rather than x64.

---


#### Unit 1   Lecture 3: Transforms 1   L3V3: TRANSFORMS 1: 3D ROTATIONS

# L3V3: TRANSFORMS 1: 3D ROTATIONS

### L3V3: Transforms 1: 3D Rotations

https://youtu.be/LazSPnaoJ_Q

> In this segment of the course we are going to talk about 3D rotations.
> 3D rotations is a topic that has engaged many of the greatest minds of
> our civilization over centuries. It's also a topic in which I have a
> special interest because my first academic SIGGRAPH paper was on
> interpolating 3D rotations. First let's review the 2D case. In that
> case we know that the new coordinate x' is given by cosine theta times
> x minus sine theta times y. y' is given by sine theta times x and
> cosine theta times y. One of the important properties of this matrix
> which we haven't talked about so far is that it's orthogonal. Most
> directly that means R transpose R is the identity (R^T * R = I) and in
> fact we can multiply that out explicitly. I am just going to use c for
> cos and s for sin. The transpose matrix will be given by cos, sin,
> -sin, cos and I have to multiply this by cos, -sin, sin, cos. Okay, so now notice what happens here. Cos times cos is cos squared, sin times
> sin is sin squared. But you know that cos squared plus sin squared is
> equal to 1, so this is just 1. cos times -sin is -sin cos sin times
> cos is sin cos. This is equal to 0.
> -sin times cos, -sine cos plus cos times sine is plus cos sine, so that will be equal to
> 0. And finally, you have -sin times -sin, sin squared, plus cos squared, which will be equal to 1. So, indeed, that's equal to the
> identity. There are also other interpretations of this. What we mean
> when R transpose R is the identity is that columns and rows are
> orthogonal. So if you look at a column like this, cos sin times -sin
> cos, -cos sin, sine cos will be equal to 0. Column dot product with
> itself, cos squared plus sine squared is equal to
> 1. Let's now consider rotations in 3D about the coordinate axes. The 2D case could be considered a special case where we're rotating about
> the Z axis. Since the Z axis therefore does not change, the matrix
> values will be 0, 0 and 1, 0, 0 and 1. And the X and Y coordinates
> will be the same as before: cos, -sin, sin cos. Similarly for rotation
> about the X axis, 1, 0, 0, 1, 0, 0, cos -sin, sin cos. Y axis
> similarly here. Since Y is equal to Z cross X, it's a little bit
> different from these where the cos, -sin, sin, cos are together but it
> still has the same form. All of these cases are orthogonal, R
> transpose R is the identity. And even in 3D because it's a matrix, it
> must follow that it's linear. We now come to the geometric
> interpretation of 3D rotations. We can think about the rows of the
> matrix as being unit vectors of a new coordinate frame. So, we can
> think of this as being the u vector, the v vector, the w vector, where
> x_u is the X coordinate of the u vector, y_u is the Y coordinate of
> the u vector, and z_u is the Z coordinate of the u vector. Similarly
> for the v vector and the w vector. When I say the u vector is the axis
> of the new coordinate frame, the vector u will be equal to x_u times
> the X direction plus y_u times the Y direction, plus z_u times the Z
> direction. The corollary of this is that given 3 orthonormal vectors,
> and orthonormality means that, this u vector dot with v vector has to
> be equal to 0, u vector dot with w vector has to be equal 0, v dot w
> has to be equal to 0, and u, v and w are unit vectors. So given any 3
> such vectors it's just a rotation of the standard XYZ coordinate
> systems and we can create a rotation matrix from there. There's also
> another interesting way of thinking about this which is that the
> rotation matrix times a point. What happens? So we can write down the
> rotation matrix in this form. So we have the u vector, the v vector
> and the w vector. All of these are vectors, times a point, right. So
> we have the point p here. Okay. So what's going to happen is you are
> going to say, u, x_u, x_p, y_u, y_p, z_u, z_p. That's just u dot p. So
> this will be equal to u dot product with p, v dot product with p and w
> dot product with p. So really, what we are doing is just taking the
> projections of the point p in this new coordinate frame. So we have u
> dot p, v dot p and w dot p. This is a very simple interpretation of 3D
> rotations that you have a new coordinate frame and you're taking the
> dot product of a point p in this new coordinate frame. To summarize,
> the rows of a matrix are 3 unit vectors of the new coordinate frame,
> rows of a rotation matrix. We can similarly construct a rotation
> matrix from any 3 orthonormal vectors. Effectively this is a
> projection of a point into the new coordinate frame. So the new
> coordinate frame, or the rotation matrix associated with it, takes the
> u, v and w coordinates to the cartesian components X, Y and Z. Its
> easy to see. So, if x_p, y_p and z_p correspond to u, then you have u
> dot p, which is u dot u, which will be 1, 0, 0. The v axis will become
> Y, the w axis will become Z. The inverse of this rotation matrix takes
> the XYZ axes to u, v and w. That's a useful property to note that a
> coordinate frame can be interpreted as stating these new coordinates
> u, v, and w, and making them equal to X, Y, and Z. The inverse can be
> interpreted as taking X, Y, and Z, and making them equal to u, v, and
> w. 3D rotations are not commutative. In particular if you rotate by X
> and then by Y it's not the same as rotating by Y and then by X. So
> here we have our teapot in the standard coordinate system and the
> thing that I am going to do is move my right. So I am going to count
> 20 steps right. 1, 2, 3, 4, 5, 6, 7, 8, 9, 10.
> 11. And similarly go up 1,2,3,4,5,6,7,8,9,10,11. And you can see here that the teapot is aligned in this way. It's essentially in a diagonal
> position from the bottom left to the top right. Take a look and
> remember where the teapot was here because now I am going to go and do
> it the other way. So, I'm going to do 11 steps like this: 3, 4, 5, 6,
> 7, 8, 9, 10, 11 and then, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11 and now
> the teapot is certainly not positioned along the diagonal from top
> left to bottom right and it actually looks fairly different. When you
> complete homework 1, I would encourage you to try similar kinds of
> experiments to convince yourself that 3D rotations are not
> commutative. This of course follows directly from matrix
> multiplications, applying R1 times R2 is not the same as R2 times R1.
> Finally the question is, can we come up with an arbitrary rotation
> formula for 3D rotations? The setup is as follows, I want to rotate by
> an angle theta, about an arbitrary axis a. This is known as the
> axis-angle form of rotations, there are many other ways of specifying
> rotations. You may want to look up quantities like, the Euler angles
> or quaternions. But, so far we are just going to talk about axis-angle
> rotations. This has particular importance for homework 1, where you
> must rotate the eye and the up direction as you move about the teapot.
> The derivation is fairly mathematical and we will be going through the
> key steps in it. The final formula is reasonably simple and is useful
> to you. So lets look at the problem setup. You have to rotate a vector
> b or a point b by an angle of theta about the axis a. If you want to
> do a sanity check on what follows, it's convenient to say b is the X
> axis and a is the Z axis. So rotation by an angle theta is just
> rotating a point on the X axis towards the Y axis. And in this way,
> you can verify that we do in fact get the right results. But we are
> going to derive it generally for b and theta. This derivation is
> carried out in 3 steps. We can regard this as the vector a, and we can
> regard this as the vector b. So it's going to rotate about a by some
> angle theta. So in this case, b will actually be rotating into the
> plane of the slides. So before we do the rotation there are some
> properties about b that we can consider. So if you look at b it has a
> component which is orthogonal to a and it has a component which is
> along a. So we can write this as the parallel and the perpendicular
> components of b along a, so that this is the parallel component and
> this is the perpendicular component. The parallel component of b just
> lies along the vector a. And therefore, it is unchanged. And this is
> just as you rotate about a given axis, that axis will remain
> unchanged. Now, we know what the formula for the vector b, the
> component along a is. And that is just going to be given by the
> quantity a dot b. So we can consider the dot product of a and b.
> Assuming that both of these quantities are unit vectors, so no
> normalization is needed. And that lies along the direction, a. So
> that's what b parallel is equal to. And b perpendicular is essentially
> equal to the vector b minus the parallel component. The second part of
> our formula says, what happens to the vector b when it rotates? And
> therefore we need to define a vector c, which is orthogonal to both a
> and b and in this case, would be into the plane of the slides.
> Remember I told you to think about the vector a as the Z axis and the
> vector b as the X axis. So if you rotate the X axis about Z you
> eventually go to the Y axis and so the vector c should be the Y axis.
> In general there will be a definition in terms of cross products. And
> we can define the vector c as being equal to a cross b. The nice thing
> is that the cross product automatically takes into account the
> parallel component and so it takes into account the magnitude of the
> perpendicular component, which is nice. So we want this a cross b but
> the amount of rotation matters. So the component along c will be equal
> to c times how much you are rotating. Only sin theta will actually be
> rotated, and then the remaining component is just going to be the b
> perpendicular component times cosine theta. And finally, we have the
> parallel component which doesn't change. Putting it all together we
> get this formula. This formula requires that we consider matrices, so
> so far we have considered the components in terms of vectors. But we
> can convert those into a representation of matrices. But first let's
> consider the parallel component, which is the component along a, which
> is unchanged. We saw here that this is going to be a dot b times a,
> but we want to write this in matrix and vector notation. So this is
> going to be equal to a transpose b times a ((a^T b) * a). All that
> I've done since this quantity is a scalar, I can move the a to the
> other side and rearrange it to get a a transpose times b ((a a^T) *
> b). I can now do the same thing for the other components so c is equal
> to a cross b and so here we said a cross b times sin theta. So this
> value is equal to a cross product of b times the sin. Right? Sin
> theta. Okay, but a cross b, we already know that cross products can be
> written in terms of this dual matrix which is "A star" (A*), takes
> into account sin theta so, a cross b is equal to A* times b and we
> have the sin theta. Finally, we come to the component along a which is
> unchanged so, this is the perpendicular component which will be given
> by the identity -a * a transpose, perpendicular will be given by b
> minus b parallel. This will be equal to the identity minus a * a
> transpose. Because we have here a * a transpose identity minus a * a
> transpose. And that gets multiplied by cosine theta. What happens to
> the perpendicular component? You get identity, minus a * a transpose,
> both multiplied by cosine theta, plus A* sin theta. And all of these
> are eventually multiplied by the vector b. So now the rotation can be
> written as some general matrix, which we'll say is some M times b (M *
> b). So, we have identity times cosine theta, which is just the
> unchanged component of the vector. And then we have, a * a transpose
> here which is one and minus the cosine theta component here. And this
> is the component along the vector a, which is unchanged, and finally
> we have the perpendicular, rotated component A* sin theta. So, finally
> this is the rotation formula for general axis-angle. If you didn't
> fully follow the derivation, that's okay. In homework 1, you only need
> the final formula, but I hope I've given you some intuition for why
> this fairly complicated formula comes about. I can also simplify that
> further and so if x, y and z are the Cartesian components of the
> vector a, then the rotation matrix can be written in this way, it's a
> quadratic form in components of the vector a and this is often known
> as the Rodrigues rotation formula.


---

Unit 1   Lecture 4: Transforms 2   L4V1: TRANSFORMS 2: HOMOGENEOUS COORDINATES

# L4V1: TRANSFORMS 2: HOMOGENEOUS COORDINATES

### L4V1: Transforms 2: Homogeneous Coordinates

https://youtu.be/dkWVytJd5_g

> Welcome to the second transformations lecture. In this lecture, we'll
> cover a whole lot more about transformations, and all of the material
> you need to get started on homework 1. This segment deals with
> homogeneous coordinates. Homogeneous coordinates are one of the most
> interesting topics in computer graphics, and really fundamental to the
> way we think about transformations. All of you have presumably
> finished homework 0 and have your compilation framework and
> environment set up. After the current lecture, you should start doing
> homework 1 because it has all of the information you need. The last
> lecture talked about 3D rotations, we will summarize those results
> here. For the homework itself you probably only need the final formula
> although it is good to understand the derivation. This lecture will
> close with the derivation of gluLookAt, which is in the last segment
> of the lecture, and that helps in clarifying many of the ideas you
> will need for homework 1. We start by talking about translation and
> homogeneous coordinates. So far we have dealt with rotations, scales,
> but we haven't dealt with the simple operation of how do you move an
> object from one place to another. Let me go back to the applet, and
> what I'll do is to make the house little bit bigger I'll include some
> scale so we will just scale it a little bit, this is really not part
> of the lecture but just to make the house somewhat bigger. I'm now
> going to show translation. I earlier showed rotations. So translations
> are very simple. In this case, I can translate by 50 in the T column
> and that's equivalent to 5 units. And that's all the translation
> consists of. So earlier my house was positioned at the center, now
> it's positioned to one side. How can I express this transformation
> using transformation matrices? For that, we come back here and I've
> written down the equations. So we have x', y', z'. There is some
> matrix we want to apply to x, y, and z. And what we want to have is
> that the x coordinate, I mean, the X position goes from x to x + 5,
> the Y position stays at y, and the Z position stays at z. So what is
> the matrix for this? Let's start exploring that. Let's just think
> about the first row, since it's only x that's being affected. So you
> know that x' is equal to x + 5. So one thinks that the first
> coordinate that multiplies x must be equal to 1. Then there is no
> effect on y, so we can just make this 0. There is no effect on z, so
> we can just make this 0, But, if were to do that, then I would say
> that, x' is just equal to x. So, I get this term, but how do I get
> this term here? How do I get the plus 5? So there have been many
> answers when I asked this question in class. And one of the ideas,
> which is not correct, (So I will start out by making it wrong), is to
> say that this quantity, for example is equal to 5 / z. And get that to
> multiply. But this is not correct because one of the key properties of
> transformations is that the transformation matrix itself remains
> constant. So it can't be a function of which location and what the
> coordinate z is. The transformation matrix cannot include the
> coordinates x, y and z. So this is a challenging problem and in
> computer graphics, it was solved by method known as homogeneous
> coordinates which enable a lot of things to happen that would
> otherwise be very difficult. The idea is simple in retrospect. You add
> a fourth homogeneous coordinate which we will use w to represent this
> fourth homogeneous coordinate. For now assume that w is equal to 1. So
> this coordinate, we will call w, which is equal to 1. The w coordinate
> is what is used for translation. So, you look at the value 5 here, it
> multiplies the w coordinate, which is currently 1, and 5 times 1 gives
> you the +5 value here. Notice that the y and z, they don't have any
> multiplication of the w coordinate because there is no translation in
> y and z. And for now, this fourth row, we will just assume as [0 0 0
> 1]. So the w' coordinate will also be equal to 1. Later when we
> consider viewing, we will play with this fourth row in order to
> include viewing transformations. That's really all that homogeneous
> coordinates are. You add a fourth w coordinate, and in this way, you
> can enable translation. But actually homogeneous coordinates allow you
> to do many more interesting things. First question is, where does the
> term homogeneous come from? And essentially, it's because the
> unhomogenized coordinates of the point is given by dividing by w. So
> you take this w value here, you divide x by w, y by w, z by w, and of
> course, w divided by w is 1. One important corollary of this is that
> any constant scale factor to a homogeneous 4-vector gives the same
> result. So essentially, it consists of all possible scales of the
> inhomogeneous coordinates of the point. In the previous slide, we
> assumed that w is equal to 1. In reality, w can be any number. For
> now, we assume it's a positive number. So w is greater than 0. And, in
> this way we can represent a wide variety of transformations. It's only
> at the end when we want to know where does this point actually lie in
> real physical world space that we have to divide by the homogeneous
> coordinate. If you multiply the 4-vector by some w value greater than
> 0 there's no effect. If you want to do a standard scale, you have to
> increase the x, y and z quantities without changing the w value. For w
> greater than 0, this is a real physical point because you can divide
> by it and you can get a real point. For w equal to 0, this is the
> point at infinity. And in fact in many formulae which would otherwise
> involve the division by 0, homogeneous coordinates allow simpler
> formulae because you can represent the point at infinity in the same
> framework. Moreover, in practical applications we often say w is equal
> to 0 to represent vectors. If you remember, vectors are characterized
> by a direction only. And so you set W = 0 so that the translational of
> components of the matrix do not apply to the vector. So what are the
> advantages of homogeneous coordinates? First it's a unified framework
> for all of the transformations we are considering, whether it's
> translation, viewing, rotation, even perspective projection in the
> next lecture. And that means that the entire graphics pipeline can run
> on the basis of homogeneous 4x4 matrices and their corresponding
> 4-vectors. Only at the final step where you have to represent a point
> of the actual screen, do you need to dehomogenize. And in fact, you
> can concatenate all of the different transformations, I move my
> object, I rotate it, I scale it, I translate it, I view it, all of
> that becomes a single 4x4 matrix. Division is a historically difficult
> operation in a computer; it can take several cycles relative to
> addition or multiplication. And division is actually essential. So if
> you consider perspective projection, you may have seen that objects
> far away appear closer. So you have to divide by the depth. The
> advantage of homogeneous coordinates is, there is only one final
> division for the dehomogenization, at the end of the pipeline. The are
> no intermediate division steps. In many mathematical formulae, the
> results are simpler. We won't go into it in detail here. But, for
> example consider intersecting two parallel lines. You have to normally
> consider the special case when the lines are parallel, your formulae
> blow up, but not in homogeneous coordinates, because the point at
> infinity, is a first class primitive in homogeneous coordinates: w =
> 0. For all of these reasons, 4x4 matrices and homogeneous coordinates are standard in computer graphics software and hardware. Let's look at
> the form for the general translation matrix. You will notice that the
> general translation matrix is just the identity in the upper left 3 by
> 3 portion. So this part is the identity and I can write it as the
> identity which is 3x3. And in fact that's what I have denoted here.
> And that's because there is no rotation applied so when the identity
> acts on x it'll be x, y and z. So it will give you this vector, x, y
> and Z. And that's exactly what we want. It's in the upper, right
> portion that we have the translation vector. So T_x, T_y, and T_z. And
> that's this portion. T. And of course there is no action on the
> homogeneous coordinate which remains 1. And therefore, this is in fact
> the point plus a translation. When considering rotations and
> translations, it's convenient to write this 4x4 matrix in this form,
> which is not quite a 2x2 matrix but in many ways behaves like that.
> And, let me just write this down again. So what you have is the
> identity. The identity is a 3x3 matrix. Then you have a translation
> and remember that the translation has 3 rows and 1 column. So the
> translation is 3 rows, 1 column. You have 0 in the bottom row, and
> that you can write as 1 row and 3 columns. And then, you just have 1
> here. So this is a convenient form. This is the form here, if you
> can't understand my handwriting, I also have it on the slide. The
> identity, translations, 0 and 1 ( [I_3 T, 0 1] ). But you should
> remember that this portion is a 3 by 3 matrix, this is a vector, this
> is a vector, this is a quantity. Nevertheless, thinking about it in
> terms of this compact form enables many formulae to go forward and we
> will use it when combining rotations and translation. Combining
> translations and rotations is intellectually interesting but also a
> very important practical problem because it's the most common thing we
> do. Typically we take an object, we scale it to the right dimensions.
> We rotate it into the right orientation, and then we translate or move
> it into the world at the appropriate location. You could also do these
> transformations in the reverse order. You could first move an object
> into the appropriate position and then rotate it. But remember that
> for now at least, rotations are always about the origin. And therefore
> it's a bit tricky as to what happens if you do the translation first.
> We will talk about both formally. In fact, these are general
> operations to do rigid body transformations. If you have a rigid body
> you can't scale it, but you can rigidly translate and rotate it and
> that is why they've received a lot of attention, in literature of many
> different fields. For now I have a translation here, that I am going
> to set back. And I am going to include the rotation. So, let's say, I
> rotate my house by, let's say, 90 degrees. Okay? Now, this is not
> probably a house you want to live in, it's on its side, but it
> illustrates our concepts. If I now put in my translation by 5 units,
> you can see that the house moves to the right as you would expect. Now
> think about it for yourselves. What would happen if I swapped the
> rotation and translation? Would the house remain in the same position,
> or would it change? And we can do that example easily here. Remember
> where the house was originally. Now I swapped, and look: it's still in
> the same orientation, it's lying on its side, but it's no longer in
> the same location. If I do first rotation and then translation, it's
> plus five units in the X direction. If I do first translation and then
> rotation, it's plus five units in the Y direction. So clearly
> translation and rotation are not commutative operations. Not
> surprising, because these are matrix multiplications. Matrices are not
> commutative. And they have different characteristic behaviors. First
> let's consider the case that may be perhaps more intuitive, where you
> first do the rotation and thereafter you do the translation. If you
> look at this equation, I have first done the rotation then the
> translation. And this TR is a combined matrix set. Now if I do the
> rotation, I have some rotation times the point P. Note that in this
> case it's not in homogeneous coordinates. It's just a standard
> 3-vector. And then I add the translation. That may seem more
> intuitive, I translated what I told you to translate, I rotated what I
> told you to rotate. So what does this become in terms of our
> homogeneous coordinates? We can use the simplified and compact form to
> get at it relatively easily. And, rotation does not involve the
> homogeneous coordinate, so I can just write this just as the rotation
> matrix. Remember that this is a 3x3 matrix. It has 0 here, 0 here, 1
> here. Translation can, as we've just seen, be written as the identity,
> which is again the 3-identity, translation, [0 1] ( [I_3 T, 0 1] ). So
> what happens if we multiply these together? So identity times the
> rotation is just the rotation itself, plus translation times 0 leaves
> us with the rotation. So we'll get the rotation here. Now come here,
> identity times 0 is 0 plus translation times 1 will give us the
> translation here. And now 0 times rotation plus 1 times 0, this is 0,
> and 0 times 0, 1 times 1 is 1. Remember, that these are still matrices
> and vectors, so rotation is 3x3. Translation is 3x1. And in fact, if
> we consider a point where again we can consider the point as being a
> 3-vector for the point and then the homogeneous coordinate and so this
> is again a 3-vector. Then rotation times point will be a rotation
> times point, plus T. So this will be equal to rotation times the
> point, plus T. And finally 0 times point, 1 times 1. So you will
> maintain the homogeneous coordinate. And, to write it out explicitly,
> you get a form like this, where you have this matrix, and this is the
> translation times the rotation. I've just written it out explicitly.
> Remember that the rotation component does not change. And then you
> have the translation, zero and one. So, it's rotation, translation,
> zero and one. And this is the homogeneous coordinates for doing the
> rotation first, and then the translation. That is for this case. So
> you rotate by 90 degrees, and in this case this is rotated and then
> you translate it. We can also consider it the other way. And in this
> case, I've swapped the rotation and translation. So, let's go back to
> our demo and let me swap rotation and translation. And now you can
> really think of it as being the same rotation. But now instead of
> translating about the X axis, I've actually translated about the Y
> axis. So, how does that come to be? And let's look at the equations
> that you get. So, in this case, I first apply my translation to P. And
> then I apply the rotations. So if I translated P, I would get P plus
> T. Again remember that, in here we are not talking about homogeneous
> coordinates, we are just doing standard vectors P plus T. I apply my
> rotation to this. So I will get RP and then I will get RT. Okay, so RT
> is the rotation applied to the translational component. An in fact, I
> can replace this by T', which is the effective translation that's
> along the Y axis. And now it makes sense because I'm rotating the X
> translation by the same rotation which is 90 degrees. So if I rotate
> the X translation by 90 degrees, I do in fact get a translation about
> Y. So, I am taking my X translation, rotating it by 90 degrees, and
> that's why I translate along Y. So the effective translation here is
> along the Y direction. For those reasons, it's a little bit
> counterintuitive and typically when you position objects, you do the
> rotation before you do the translation. But of course there is no
> fundamental limitation on that and there are some cases where you want
> to translate first. Even in the derivation of gluLookAt, that will
> come up. And so you then end of getting this effective translation.
> Apart from that the matrix should be the same but we can multiply it
> out explicitly. So, I can write down the rotation matrix as we saw
> earlier as [R 0, 0 1]. And I can write down the translation matrix as
> [I_3 T, 0 1]. So now if I multiply these together, you get rotation
> times the identity plus 0 times 0. And that will be equal to the
> rotation. Rotation times translation plus 0 times 1, and that will be
> my component rotation times translation, which is equal to this T
> prime here, okay? 0 times the identity plus 1 times 0 is 0. 0 times
> translation plus 1 times 1 is 1 and this is the final matrix that you
> will get. Here, I've written it down explicitly so you'll have the
> rotation times the translation, and what you'll end up with is the
> rotation 0 and 1 and this is the 3x3 matrix of the rotation multiplies
> the 3-vector of the translation and you'll end up with this effective
> translation.


---

#### Unit 1   Lecture 4: Transforms 2   L4V2: TRANSFORMS 2: TRANSFORMING NORMALS

# L4V2: TRANSFORMS 2: TRANSFORMING NORMALS

### L4V2: Transforms 2: Transforming Normals

> In this segment, we will talk about transforming normals. So far, all
> of our activity has been about transforming geometric objects and
> points on the surface. However, the surface orientation of the surface
> normal is also critical for computer graphics. One important use is in
> lighting. The intensity you see from the surface depends on the angle
> between the light source and the surface normal. For highlights on the
> surface it depends on the angle between the viewer, the surface normal
> and the light source. And the normals do not transform the same way as
> surface positions. To see why, we can look at this diagram. Here, I've
> just shown the effect in 2D, and that's all you need to really
> understand it. I have a rectangle, and of course, the surface normals
> are pointing straight upwards. I now apply a shear to the rectangle,
> and so it becomes a parallelogram like this. But of course, the
> surface is normal on the top is still pointing upwards. However, if I
> were to apply the same transformation as I apply to the geometry,
> imagining the normals attached to the geometry in this part of the
> geometry of the object. Then when I shear it, what is going to happen,
> is that it is going to move, because I'm moving points here more than
> I'm moving points here. And so, while this point will move a little
> bit in the direction of the shear, this point will move more. And so,
> the normal will appear tilted, when that's not really the case. So
> therefore, we need to derive the correct transformation for the
> surface normals. And we will go through some algebra, which is the
> easiest way to see how they deform. If you want to think about this,
> also think about the transformations in a circle when it's stretched
> into an ellipse. The normals will not transform the same way as the
> geometry. In fact, they'll transform in the inverse way in a certain
> sense. So, to find the normal transformation, we consider a point on
> the surface, and we consider the geometric location around it. So, we
> consider a plane around the point, here is the point, here is the
> normal, here are some points on the plane, which we consider the
> tangents. Tangents are actual geometric locations on the surface and
> they transform just as the same transformation matrix on the surface,
> so M times t. Normals transform with another matrix which we'll call
> Q. And the question is, what is Q equal to? One of the important
> things we know is that the normal has to be at 90 degrees to the
> tangents, so its dot product with respect to the tangents has to be
> equal to 0. This is the basic definition of a plane or the definition
> of normals. So n dot t has to be equal to 0. Now, the question is, we
> want to solve these equations, and we want to find what the matrix Q
> is. But, this is the condition, n transpose T is = to 0 (n^T t = 0).
> So n is equal to QN. And so let's transpose that. So let's look at QN
> transpose ((Qn)^T). Now when you transpose, you transpose the
> individual elements. And you invert the order in which they apply. So
> this will be equal to n transpose times Q transpose ( (Qn)^T
> = n^T * Q^T ). And t will be equal to Mt. So we will have this times Mt is equal to 0. So I've just reproduced that here. So I have n
> transposed, Q transposed Mt is equal to 0 ( n^T * Q^T * Mt = 0 ). And
> this implies that Q transposed M must be equal to the identity ( Q^T *
> M = I ). This is because this must hold for any n and t in order to
> get the original condition that n transposed t is equal to 0. So of
> course, if Q transposed M is equal to the identity, it's very easy to
> solve for the matrix. And we have that Q is equal to M inverse,
> because I multiplied by M inverse on both sides and then I have to get
> rid of the transpose and so I take M inverse transpose ( Q = (M^-1)^T
> ). One point I want to make very clear, since we've just had the
> discussion of homogeneous coordinates, is that this inverse
> transposition is applied to the upper 3x3 matrix only. So it's applied
> to the upper 3x3 matrix only. It doesn't really apply to the
> homogeneous coordinates, and in particular the normal, being a vector,
> isn't really acted on by translations. And so, what you do to the
> translational coordinates doesn't matter. But, in order to change this
> vector you do have to apply this inverse transpose to the upper left
> 3x3, which includes things like rotations and shears, and so I'll also
> say there is no effect of translation, right. So no T translation
> applied. Finally, we have the formula here. Q is equal to M inverse
> transpose ( Q = (M^-1)^T ). And this formula must be applied to all
> surface normals.

---

#### Unit 1   Lecture 4: Transforms 2   L4V3: TRANSFORMS 2: ROTATIONS AND COORDINATE FRAMES

# L4V3: TRANSFORMS 2: ROTATIONS AND COORDINATE FRAMES

### L4V3: Transforms 2: Rotations and Coordinate Frames

> In this segment we are going to revisit rotations in both 2D and 3D,
> and talk a little bit about coordinate frames. So far, all of our
> discussion has been in terms of operating on points. But one can also
> change the coordinate system and in fact, these are equivalent ways of
> thinking about transformations. For example, if I move towards you, it
> can be interpreted in two different ways. Either you think of the
> coordinate system as anchored to yourself and I am actually moving
> towards you, or you think of the coordinate frame moving backwards and
> moving away from me. So let's look at this with an example. Here we
> have a point which is located at 2 units along the X axis, 1 unit
> along the Y axis. I can now translate that point to the left, so I can
> move it to the location (1,1) in both axes. So this would be a left
> translation. I can also see this as a change in coordinate frame,
> where the coordinate frame moves to the right. And so the point item
> moves 1 unit to the left, or the coordinate frame moves 1 unit to the
> right. And both of these interpretations are equivalent, and you can
> use the interpretation that's more useful in a specific task. So the
> reason I brought this up is that in many cases, you want to define a
> coordinate frame which is anchored to a specific person, to an object,
> to the world, etc. And in many cases, you want a particular physical
> location in the world to be transformed between coordinate frames. In
> general, coordinate frames can have both translation and rotation. The
> center can be somewhere in the world and they can be transformed by
> orientation; their axes can be different. So here you have the world,
> and you have an origin in world space, x and y axes. In the camera
> coordinates you have some eye location in u and v, which are the
> equivalent for x and y. So let's look at a point p, and we want to
> find the coordinates of a point p. So in world space, it's let's say 2
> units along the x axis, 0.9 units along the y axis. In the same point,
> in the camera coordinates, it's different. So it's some location along
> u. Let's say .5 along u, and -.6 along v. And in many cases, one wants
> to do this. One has a geometric location in the world, even in
> homework 1 on your teapot. And one wants to figure out where it lies
> in camera coordinates, that has to take into account both the
> rotational coordinate system of the camera, as well as where the
> camera is located, and what the eye coordinates are. Let's go a little
> bit further and talk about new interpretation of 2D rotations. If you
> remembered my derivation of 2D rotations, I said a point P moves to
> P', and the point P makes some angle alpha with the axis. The angle of
> rotation is theta. And so you eventually make an angle of alpha plus
> theta. If you write out the coordinates x and y and you simplify the
> trigonometric identities, eventually you get a rotation matrix like
> this which is which is cos theta times x minus sin theta times y sin
> theta times x plus cos theta times y. So this is your rotation axis.
> Of course following the key of rotating points versus rotating
> co-ordinate systems, one can think about the point as being fixed, but
> the coordinate system rotating in the inverse way. And, indeed, this
> is what the coordinate system rotation looks like. This is the new u
> axis; this is the new v axis. And the coordinate system is rotated
> clockwise by theta, whereas the point was rotating counterclockwise by
> theta. So what are the coordinates of the new u and v directions? And
> we'll derive these in a moment. If we look at what the x coordinate
> here is, this so since the axis are of unit norm, this distance is
> going to be cosine of theta. And this length is going to be minus sine
> of theta. So, the u coordinates are actually going to be given by cos
> theta minus sine theta, that's u. And v coordinates will be given by,
> this angle will again be equal to theta and so you can see along the x
> direction, the v coordinate will be given by sine theta, so I can
> write this as sine theta, and along the y direction this will be
> cosine of theta. And in fact, that's what this is. Sine theta, cosine
> theta. So the rows of the rotation matrix can really be regarded as
> the coordinates of the new axes. And in fact that's what it is. So the
> uv coordinates of the new axes are equal to cos theta x minus sin
> theta y, sin theta x cos theta y, of the old axes. And this leads to
> the nice geometric interpretation of 3D rotations which we also talked
> about earlier. Which is the rows of the matrix are 3 unit vectors of
> the new coordinate frame. And one can construct a rotation matrix from
> any 3 orthonormal vectors. And in fact, the u coordinates are just
> x_u, y_u, z_u. v coordinates similarly and w coordinates. Finally I
> want to briefly revisit the axis-angle formula that we derived in the
> previous lecture. And I won't go over all of the derivation before,
> but the essential parts are there is a part which is the identity of
> cosine theta, then there's the a * a transpose part, then there's the
> dual matrix and the cross product part. I mainly put this slide up so
> that it can be useful for you for revising when you do homework 1. The
> identity 1 minus cos theta times this matrix. It has quadratic
> components and then sin theta times this cross product matrix. That
> will be what the rotation matrix looks like. All of this gives you
> enough material that we can actually derive the 4x4 matrix for
> gluLookAt which is a large component of what you need to do in
> homework 1.

---
#### Unit 1   Lecture 4: Transforms 2   L4V4: TRANSFORMS 2: DERIVATION OF GLULOOKAT

# L4V4: TRANSFORMS 2: DERIVATION OF GLULOOKAT

### L4V4: Transforms 2: Derivation of gluLookAt

> In this final segment of lecture 4, we have achieved all the tools
> needed to derive gluLookAt, which is a key OpenGL component for
> viewing. And it's really a case study, of course immediately relevant
> to homework 1, but really a case study on how you can use all of the
> ideas you have to derive this relatively complicated 4x4
> transformation matrix that can be used to view objects and position an
> arbitrary camera in the world. The function we are going to talk about
> positions the camera, and is therefore fundamental to how we look at
> images. Let's talk about the parameters for a moment. So you have the
> x coordinate, y coordinate and z coordinate of the eye. You have the,
> x, y and z coordinates of the center, which is where it is looking at.
> And, you have an up vector of the camera, which is, what is the up
> direction of the camera? And that is important for determining what
> parts of the image are on the X axis and the Y axis. What is the
> orientation of the image with respect to the world? It corresponds to
> rotating your camera. The eye location corresponds to where you place
> your eye, or your camera. Whereas, the up direction corresponds to the
> orientation or heading of the camera, or equivalently how you rotate
> your head. And really the key thing is, this combines many of the
> concepts discussed in the last two lectures and gives you a practical
> example of how you solve problems. It involves 3 main steps to derive
> the matrix. First we need to create a coordinate frame for the camera.
> Then we need to create a rotation matrix corresponding to the camera's
> coordinate frame. And finally, we need to apply a translation for the
> camera, or the eye location. In the basic math lecture, and we talked
> about vectors and orthonormal basis frames, we introduced the notation
> and the way in which we can create the coordinate frame. So
> essentially you have a vector a and a vector b, in this case given by
> the direction of u, which is the difference between eye and center,
> and b which is the up direction. But of course these might not be
> orthogonal nor unit norm, and you also need to find the third axis of
> the coordinate frame. So what you do is, first you create the w
> vector, which is just normalizing a, and that's equivalent to Z axis.
> And then of course you have to remove the components of v which fall
> along w, and instead of doing that explicitly, a more elegant way is
> to find the u vector which is b cross w and so the cross product
> automatically removes the appropriate components. And finally, you can
> create v as w cross u which is an identity that must hold in an
> orthonormal coordinate frame. So we will go back to this early
> construction we saw in the basic math lecture. In order to create the
> coordinate frame, of course you have to know what is my a and b that
> I'm given, and so I've rewritten what w, u and v are here, but I need
> to know what's a and b. And let's go back to our problem statement. We
> want to position the camera at the origin, looking down the -Z
> direction. In OpenGL, you always have a camera at the origin looking
> at (0,0,-1). So it's looking at -Z direction. Therefore, center - eye,
> you want to move that to the -Z direction. Therefore, the +Z direction
> will be given by eye - center. And that's what the vector a is given
> by, eye - center. The vector b is then simply the up vector, and those
> are your two vectors, a and b, eye
> - center and eye. So from that, you can compute the vectors u, v and w using the formulae discussed earlier. But the main reason for doing
> that is you want to create a coordinate frame and a rotation matrix.
> So then we go back to what we discussed earlier in this lecture and
> also in the next lecture, in previous lecture, that the rows of the
> rotation matrix are the 3 unit vectors of the new coordinate frame. So
> given be u, v and w, you can define, you know the x, y and z
> coordinates of u, x, y, and z coordinates of v, x, y, and z
> coordinates of w. The rows of the matrix of are the vectors u, v and
> w. And so, you have constructed a rotation matrix for the camera. The
> final step is that you need to apply a translation for the camera, or
> the eye location. And this, is a little bit of a trick question. Do
> you do the rotation first or the translation first? And that's what we
> talked about earlier in the lecture. The important point to note is
> that you cannot apply the translation after the rotation. Think about
> it, you have a camera. And, so, you can think about it in 2 steps.
> First the camera is looking down the -Z axis. It's moved to the
> appropriate location in the world, so you have to apply to the inverse
> translation to the world. And then, it's positioned appropriately,
> which corresponds to the rotation. So the translation must come first
> to bring the camera to the origin before the rotation is applied. How
> do we combine translations and rotations? Again, I'm just repeating
> slides earlier in the lecture. The main point of this segment is to
> show easy application of the way you can use all of the knowledge I've
> been talking about. So if I do translation first and then rotation I
> have an effective translation, which is rotation times translation. So
> the rotation matrix times the translation vector. In this case, the
> translation vector is the eye coordinate or really the -eye
> coordinate, because I have to do the inverse translation to the world.
> And the rotation matrix are the u, v, and w coordinates of the new
> coordinate frame. Take the rotation matrix, and I take the translation
> vector, which is -eye. And now, I multiply these together. So, of
> course, the rotation part doesn't change, and I'm not interested in
> that. So I'll just talk about how the translational components will
> change. And you notice here, I'm going to have x_u * -e_x, y_u * -e_y,
> and z_u * -e_z. This just corresponds to a dot product of the vector
> u, and the vector e, of course with the negative, and therefore these
> things will become, -u dot e, -v dot e, and -w dot e. Of course, do
> not confuse this w vector with the w homogeneous coordinate, which is
> just 1 in this case. In fact, in the earlier segments, we did derive
> this form, for this is what happens, that when you rotate a particular
> vector, it's equivalent to considering its projection in terms of the
> new u, v and w. And just writing this down explicitly, we derive the
> formula shown here. And this is the final form of gluLookAt. Some
> components of this you will need in homework 1.

--- 

#### Unit 1   Lecture 5: Viewing   L5V1: VIEWING: ORTHOGRAPHIC PROJECTION

# L5V1: VIEWING: ORTHOGRAPHIC PROJECTION

### L5V1: Viewing: Orthographic Projection

> So far, we have considered transformations that are entirely in 3D. So
> they deal with how do you take an object in the 3D world and place it
> somewhere else in the 3D world. In this lecture we're going to talk
> about viewing, because ultimately we look at computer graphics images
> that are 2 dimensional, and therefore we have to take this 3D world
> and project it into a 2D image. While we're talking about computer
> graphics, we are of course inspired by similar processes that occur in
> the human eye and in real cameras. We have seen transforms so far
> between coordinate systems but of course all of that is 3D. How do you
> go from 3D to 2D, and how do you project the 3 dimensional space to
> the 2 dimensional space is the fascinating topic that this lecture is
> about. I'm going to start off by showing you a demo with this
> projection tutorial. These come from Nate Robins' OpenGL tutors. And
> if you just search on the web for that, you will see many interesting
> tutorials that give you a good understanding of several aspects of 3D
> computer graphics, and also how to implement them in OpenGL. So here,
> we have our projection tutorial. And so what it shows is the world
> space view on the left, and the actual image that you see on the
> right. So what I can do here, is that I can increase the field of
> view. And, as I increase the field of view, you'll see that the man
> becomes smaller; as I decrease the field of view, he becomes larger.
> And that's because I'm looking at a smaller region. So that is one
> parameter of my viewing transformation. I can also change the aspect
> ratio, which affects the width to height. And, finally I have the
> zNear and zFar which are the near and far clipping planes. They don't
> really do anything until I pass them through the object, and then you
> lose some of the object. In this lecture, we are going to understand
> all of these concepts, and derive the matrices that are actually used
> in OpenGL. To summarize what we've seen so far, we've seen
> transformations, translation, rotation, scale, and how to put them
> together. All of this is done using 4x4 homogeneous matrices. And so
> far, they were motivated primarily by the ability to capture
> translation. However, 4x4 matrices are also useful to capture viewing.
> And, indeed, there is a unified way to write the entire transformation
> pipeline. The last row in these matrices has always been so far [0 0 0
> 1], just keeping the w coordinate unchanged. For viewing
> transformations, we will play with this last row, as well as other
> parts of the matrix. This segment deals with orthographic projection,
> which is the simplest one. And then we'll deal with perspective
> projection, which is the most common way in which images are created.
> First, consider the problem formally. You have 3 dimensional space,
> and you want to project it down to 2 dimensions. That's essentially
> the meaning of projection. One obvious way of doing that would be to
> take your 3 coordinates in the 3 dimensional space, and drop one of
> them to a 2 dimensional space. Indeed orthographic projection, at a
> high level is just taking X, Y, Z of your 3D space and dropping the Z
> coordinate, so you get X, Y on the screen. It preserves straight
> lines, which is one of the main advantages of it, and it looks
> something like this. So, one of the characteristics of orthographic
> transformation is that parallel lines remain parallel. Some of you
> here may remember if you see images of, for example, railroad tracks.
> Those are clearly parallel lines, but in a standard camera image they
> will seem to be getting closer together till they meet in the far
> distance. You of course never see them meet, they meet only at
> infinity, but they get closer to each other. That's because the image
> was created using perspective projection. With orthographic
> projection, the parallel lines remain parallel. And, this is useful
> for many technical drawings to convey the view of the object. And you
> may, for example, take an orthographic view along each of the X, Y,
> and Z axes. So here I've drawn an example of the cube, and you'll see
> with the perspective transformation, parallel lines are no longer
> parallel. The cube is somewhat distorted. Whereas in the orthographic
> case, we maintain those parallel lines. What we're going to talk about
> now is the general form of the orthographic transformation. It's
> something known as glOrtho. And we'll just go over it as a warm-up to
> derive the formula for gluPerspective for perspective transformations.
> The basic idea for the general orthographic transformation is that you
> have a cuboid in world space. So here is your cuboid. You want to map
> that cuboid first to the center it, and then finally map it down to
> the unit cube, and indeed all of the transformations we'll see,
> gluOrtho, gluPerspective essentially compute a mapping of some region
> of the world down to unit cube. Of course, you can argue that this
> mapping is still 3 dimensions so, what's going on? But the idea is
> that once we map it to the unit cube, then we can just drop the Z
> coordinate and look at the XY coordinates. So, how do we go about it?
> The first thing is that we need to define the axes of the cube. And
> so, since it's a cuboid which is parallel to the X, Y, and Z. The left
> and right components are just l and r, and that corresponds to these
> faces, so this face here, this face here, that's the left and right.
> The near and far already lie along the Z axis. So the near plane is
> the closest location and the far plane is the furthest location. And
> then we have top and bottom so, top and bottom. So I am just reprising
> the different steps that you are going to take, where you first center
> the cuboid and then you scale it into the unit cube, and for each of
> these steps we can derive the appropriate matrices. And the idea is as
> follows. I have my cuboid, I am going to draw it here. And so firstly
> these are l and r. l and r, and this must go to something that is
> centered. And so we want it to have the same length. But now, this
> point must move to the center. And, of course, the translation that
> will make that happen, is to consider the central location here, which
> must be equal to (l + r) / 2. And therefore the translation will be
> the negative of this, in order to bring this to the center. Similarly,
> for top and bottom, you will have minus, top, plus bottom, over
> 2. And, that will be the case for the near and far planes as well. I'm not going to write that down, but that will be minus far plus near
> over 2. The next question is what happens to the scale, and of course
> the scale will depend on the inverse of this length, so this is the
> translation, and now let's look at the scale. In this case, you will
> look at this total extent, and will want to scale that into the unit
> cube. In this case, the unit cube goes from -1 to +1. So this total
> extent will go from -1 to +1, which is a total of 2 units. So of
> course, the scale will be 2 units divided by the original length. So
> this will be equal to 2 / (r - l). 2 divided by r minus l, and
> similarly 2 divided by t minus b, and 2 divided by far minus near. So
> let's look at what this look like, the scale matrix is 2 / (r - l), 2
> / (t - b), 2 / (f - n). Notice that the scale comes second, the first
> step is the translation. And the translation is left plus right
> divided by 2 with an minus sign. Top plus bottom divided by 2. Far
> plus near divided by 2. And so far I've left the homogeneous
> coordinate row the same. One can multiply this out and it's easy to
> see what happens. It's similar in many ways to what we did if you do
> translation first and then rotation. So the upper left 3x3 remains
> from the scale, and you can see that quite clearly. But for the
> translation, you have to multiply the scale by the translation. And so
> 2 and 2 cross out, but you get minus l plus r over r minus l. And that
> can be within as l plus r over l minus r. As an exercise you might
> want to multiply this out, together, yourself. There is one final
> change that needs to be done to get the glOrtho formula. Which is that
> in Open GL, the convention is that you're looking down the -z axis.
> Therefore, n and f are both negative numbers. So n is closer than f,
> and it's a smaller negative number than f. However, when you specify
> the arguments, you specify n and f as positive values. And therefore,
> in the formulae, you have to replace n by -n, and f by -f. Which, all
> it does is it changes 1 sign to negative. And, in particular, the
> formulae for M is, again, the upper left 3 by 3 doesn't change. It's 2
> by r-l, t-b, f-n. And here, r+l, r-l, top plus bottom, top minus
> bottom and so on. But there is one sign change that happens when you
> replace far and near by their negative values, which is that this sign
> changes. And that's the final formula for glOrtho. Why have I
> introduced the derivation of these formulae, gluLookAt in the previous
> lecture and glOrtho in this lecture? Because, eventually, when you
> actually design a scene using OpenGL, what it does is it takes all of
> the geometric points, and it transforms them by a 4x4 matrix. Of
> course, you can, and if you're writing in OpenGL, just specify glOrtho
> with some intuitive parameters. But, of course, the goal of this
> course is to understand how the 3D pipeline works. And therefore, you
> need to understand the basics of orthographic and perspective
> projections, and how one creates 4x4 matrices that one actually uses,
> from them.


---

#### Unit 1   Lecture 5: Viewing   L5V2: VIEWING: PERSPECTIVE PROJECTION

# L5V2: VIEWING: PERSPECTIVE PROJECTION

### L5V2: Viewing: Perspective Projection

> We now come to perspective projection. If you look at objects around
> you, whether it's with your eyes, whether you look at computer
> graphics imagery. Even if you look at art after the Renaissance. We
> see that objects that are further away become smaller. In fact, a
> common experiment is, you place a quarter in front of your eye, and
> you can block out the moon or the sun, when, clearly, they're much
> bigger than the quarter. Furthermore, if you look at something like
> railway tracks, you will see that the lines, even though they are
> parallel, seem to converge in the distance, although they never
> actually meet. This is perspective projection where you have a center
> of projection which is the camera, or the eye location. And the
> geometry is as shown here. This is your screen, and the line AB will
> project onto A'B'. Of course, the further away it is, the smaller it
> will appear when projected. This is the standard projection model that
> is used everywhere, not just in computer graphics. And we are going to
> talk about the mathematics required to make that work. Consider this
> overhead view of our scene. This is the eye, or the camera. So let me
> note that down. This is the eye. Here we have our screen, or our
> image. And so, let's say this is the image. We have some location in
> the world (x, y, z) that projects to some location (x', y', d). The
> question is, what are the coordinates of this point? So of course the
> formulae for x' and y' are similar. We can just do one of them. The
> screen is assumed to be a distance d away, and the world space object
> is a distance z away. Now, the triangles are similar, so this triangle
> is similar to this whole triangle, and therefore the length ratios
> should be similar. So I can say that d / x' is equal to z / x. Let me
> just write that down. Of course what I really want to solve for is,
> what is x' equal to? And so x' I can bring here and it will be equal
> to d * x / z. And so this implies that x' will be equal to d
> * x / z. This division by z is really critical. That is what ensures that the object gets smaller the further away it is from the screen.
> And of course, we cannot divide by z using standard matrices. But
> that's where homogeneous coordinates really become useful. Because to
> dehomogenize, you divide by the fourth coordinate. And one can create
> the matrix so as to put z in the fourth coordinate. Just bringing this
> up here, you can say I just wrote it the other way. I said d / x'. But
> one can write it in this form. You have x' is equal to d * x / z. And
> y' is equal to d * y / z. So what does the 4x4 matrix look like? X and
> Y values do not change, but we are playing with the fourth coordinate
> here. So what I am going to do is that I am going to try to write this
> times some [x, y, z, w] to show you what happens. This will be equal
> to. So the x coordinate doesn't change. And so we can just write this
> as x. We can just write this as y. And initially, let's say w is equal
> to 1. Okay, so what happens to Z? It doesn't change either. So the
> only change is in this 4th coordinate, where the w value I've just
> multiplied by zero. So it's not even relevant. But what I'm doing is
> I'm taking -z / d here. So -z / d. Now, if I dehomogenize this, you
> will see that x will be multiplied times d / z, y will be multiplied
> times d / z, as we wanted. And, in fact, the z coordinate which I'm
> going to drop. If you also multiply it by d / z, it will be equal to
> d, which is just a constant, which is where the image plane is. Now,
> of course, the question is, why is the minus sign. Again, OpenGL
> convention, you're looking down the -Z axis. And so the focal plane is
> at -d. So again, I went through that verification already. You can do
> this formula, and it's [x, y, z, -z / d]. If you multiply it out
> you'll get -d * x / z, -d * y / z, -d and
> 1. And in fact this is exactly what you want to do to in order to get perspective projection working. The next segment will deal with the
> derivation of gluPerspective, putting together the concepts we have
> talked about so far for perspective projections to see how the final
> matrix in OpenGL, with all of its complexities, is created.

---

#### Unit 1   Lecture 5: Viewing   L5V3: VIEWING: GLUPERSPECTIVE

# L5V3: VIEWING: GLUPERSPECTIVE

### L5V3: Viewing: gluPerspective

> At the end of the last lecture, we derived gluLookAt transformation in
> order to place objects in the 3D world for a given camera. In this
> lecture, we're going to talk about the gluPerspective transformation
> which transforms the 3D world appropriately to place objects onto the
> screen. The entire transformation pipeline will include first, a
> gluLookAt or equivalent camera transformation, and then the viewing,
> or the projection transformation. Let's go back to the projection
> tutorial. We'll notice here that gluPerspective has 4 commands.
> gluLookAt below has eye, center and up. We already saw this. And
> again, you can increase the field of view; you can play with the
> aspect ratio. You can change the near clipping plane. You can change
> the far clipping plane. So what are all of these different variables,
> and how do they affect the gluPerspective matrix? Fundamentally, we
> have a viewing frustum in gluPerspective. Remember that in glOrtho,
> this was just a cuboid. Because, objects, they stay in the same
> location regardless of depth. The size remains the same. However, for
> perspective projection, further away objects become smaller. And so
> what you really have is a viewing frustum. So we can think of this as
> being the eye and you can complete the frustum in this way. But any
> object that lies below the near plane, you block out. And similarly,
> any object that lies beyond the far plane you block out. That's why
> you're specifying the near plane and the far plane. And that's why you
> have a frustum. The next parameter is the field of view, and that's
> fairly obviously defined. In fact, it's the field of view in the Y
> direction because the X and Y field of views could actually be
> different. And you have a screen which has some width and some height.
> The aspect ratio is the ratio of width to height. We're not going to
> talk very much about it, but it does need to be considered in deriving
> the appropriate formula. The gluPerspective command takes in a field
> of view in the y direction, the aspect ratio, and positive values for
> zNear and zFar. So although you're looking down the -Z axis, these are
> distances that are positive. So the field of view and the aspect ratio
> control the field of view in the x and y directions, and zNear and
> zFar control the viewing frustum. Here is the overhead view of our
> screen again, and we will be interested in computing the quantities
> theta and d. This quantity is theta, and this is given simply by the
> field of view in the Y direction divided by 2. So the total field of
> view is 2 * theta. So, this quantity theta we can write as the field
> of view y divided by 2. Very simple. What is d equal to? Just from the
> geometry of the situation we want to map things again onto the unit
> cube. So this is 1 unit. And from trigonometry we know that tan theta
> is equal to 1 / d, which means d must be equal to cotangent of theta.
> So d we'll write as cot theta. I've just noted that down again here on
> the slide. We now need to find the matrix corresponding to this. And I
> have written it down in the simplest form. The -1 / d here,
> corresponds to the perspective transformation. So this is just your
> standard perspective 1 / z transformation. And this is what requires
> that the z coordinate divide by d and so you get smaller the further
> away you are. Finally, the aspect ratio is taken into account here,
> and in this way you can handle different aspect ratios. Since we are
> in homogeneous coordinates you can multiply all of this by a constant
> factor without affecting the matrix, and therefore you just multiply
> the whole thing by d. In this way, this becomes -1, and the other
> coordinates change accordingly. So we have d by aspect. This becomes
> d. And here, I've written these as A and B because we're going to play
> with this lower 2x2 matrix in order to get the near and far planes to
> map properly. This is all that is required to get z to map properly,
> so we don't care about x and y. We only care about z and w for the
> mapping of the near and far planes, which we'll get to next. Normally
> when I talk about homogeneous coordinates, I say it's a 4-vector. x,
> y, z and w. However, you can also add a homogeneous coordinate to a
> single coordinate, z in this case. And so for simplicity, I have just
> written z and w. I've omitted x and y because we've already found the
> matrix form for them, and they are not affected by this mapping. So
> this is, I'll just write down, this is the w coordinate. So let's see
> what happens here. I will get Az+ B. And this will be -z. Note that
> this is still in homogenous coordinates. So if I have to dehomogenize,
> I have to divide by this -z. And I'll get -A - B / Z. So I've just
> noted that down here. And now we have a system of simultaneous
> equations that we have to place to consider the near and far planes at
> the appropriate location. When z is equal to -n, remember that we are
> looking down the -Z axis. We want this quantity to go to -1, because
> we are mapping to the unit cube. And when z is = to -f, you want this
> quantity to go to +1. Because, again, we are mapping from -1 to +1.
> So, z is equal to -n. I put -n in here. And therefore, I have that -A
> + B / n is equal to -1. Now, z is equal to -f, is plus 1, I put z is equal to -f in here, and I get similarly an expression like this, -A +
> B / f is equal to +1. Here, I have a system now, of simultaneous
> equations for A and B. And so I can solve this. I can subtract these
> equations, and I'll get a formula for B. I can appropriately scale and
> multiply them to get a formula for A. I won't go through the algebra
> here. You can work it out as an exercise. The important thing is to
> write down the simultaneous equations, which I just showed you. And
> eventually, you get a formula like this. A = -(f+n)/(f-n), B =
> -2fn/(f-n). That completes the derivation of the gluPerspective matrix. Indeed, in homework 2, you will be, in addition to using
> gluLookAt, you will also program in yourself the gluPerspective
> matrix. Finally, I want to do two things. First, I briefly want to
> discuss the nonlinear mapping in z. And second, I want to show you a
> summary of the entire transformation pipeline in OpenGL, which in the
> last few lectures we have been getting to parts of. I first note that
> the mapping of z is non-linear, and I've written down again what
> happens to the z and w coordinates and when you dehomogenize you get
> -A - B / Z. The nonlinear mapping has A proportional to 1 / z. This nonlinear mapping is interesting. Of course, in principle you don't
> need to map it this way. And in fact, with the advent of programmable
> shaders you could in principle take over the z-mapping to whatever you
> wanted. Some of the more ambitious of you might want to play around
> with that in homeworks 1 or 2. However, all of the mappings that have
> been proposed in the literature have these kinds of nonlinearities.
> And it has an advantage, which is, that it handles a broad range of
> depths. 1 over infinity is 0. 1 over 100 is .01. They're very similar.
> You handle the full range. And so, you can have depths from 10
> centimeters to 100 meters. And in many computer graphic scenes, you
> do, in fact, have this range of depth. However, and this is a major
> challenge. The depth resolution is not uniform. The depth is intended
> to be the maximum near the near clipping plane. And for those of you
> who can follow along with this, one quick way of seeing this if you
> differentiate this, this corresponds to depth resolution. It will be
> proportional to 1 / z^2. And of course 1 / z^2 is small near the near
> clipping plane, and rapidly degrades as you get further away. So, one
> common mistake that people write in writing their programs is to set
> the near clipping plane to 0, the far clipping plane to infinity. You
> say, "I don't want to deal with the frustum. I'm perfectly happy
> considering all objects." This is a problem, and in fact, we'll show
> in a later lecture, I'll show actually programming this in and how it
> leads to garbage. Because all of the depth resolution then is at 0,
> then in fact for an object at any positive depth value, you will have
> zero resolution. When you have limited resolution, all objects go into
> the same depth bin because in practice you have a finite quantization
> in the depth buffer and therefore, effectively you can't resolve
> depths. So therefore, do not set your near clipping plane to zero.
> With the far clipping plane, you have much more flexibility because it
> goes as 1 / z, so one over infinity or 1 / 10,000 doesn't really make
> much difference. But the near clipping plane is more sensitive and it
> should actually be set to where the geometry in the scene is. Let me
> finally summarize the whole viewing pipeline. I acknowledge Greg
> Humphries for originally providing this slide. You start in model
> coordinates over here. And then you apply a transformation to the
> model. This is scale translation, rotation, it's a 4x4. You eventually
> get to world coordinates. Then you apply the camera transformation,
> gluLookAt, which is what we ended the last sequence of lecture
> segments with. Now you have things in what are known as eye
> coordinates. So far, for just projecting geometry, the distinction of
> each of these individual stages model will die, it's not important,
> because you concatenate the transformations together. But, one of the
> critical things is lighting, which we'll talk about in, a few lectures
> from now. That is performed in eye coordinates. So lighting is
> performed in eye coordinates, that's important. Because lighting is a
> 3D concept, and you don't project the scene before you perform
> lighting. Okay. So, this highlighted region is the perspective
> transformation gluPerspective which is what this lecture has been
> about. And once you go through the gluPerspective transformation, so
> remember that you will apply gluPerspective to the results of
> gluLookAt, the net transformation matrix will be the projection matrix
> times, what's known as the ModelView matrix or gluPerspective
> * gluLookAt. Then you go into screen coordinates, so you're in what's also known as normalized device coordinates. It goes from -1 to +1.
> It's a cube. After that you have to go through the viewport
> transformation, which goes to the actual window you're considering,
> and finally you go to the device coordinates. These 2 steps we don't
> talk about very much, but notice that if you look at the programs they
> will have a glViewport command. And essentially once you're in the
> unit cube you still have to get to the appropriate location in your
> screen and position the window appropriately on your monitor. And
> that's what these two things deal with. As far as this lecture has
> been concerned, the past two lectures have dealt with the model
> transformation and the camera transformation. This lecture has dealt
> with perspective. And all of these come together in the viewing
> pipeline.

---

#### Unit 1   Homework 1   HW1: Introduction

# HW1: Introduction

### Homework 1: Transformations

#### Introduction

