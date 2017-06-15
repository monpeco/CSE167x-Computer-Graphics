 Unit 2   Lecture 6: OpenGL 1   L6V1: OPENGL 1: OVERVIEW
 
 L6V1: OPENGL 1: OVERVIEW
 
 https://youtu.be/MksaEc1y0Us
 
 > In this sequence of lectures, we are going to take a somewhat
> different approach and study the workings of the OpenGL language. What
> we're going to do is use this as a vehicle in which to understand
> systems 3D graphics programming. And the way in which you can play
> with vertex and fragment shaders and other aspects of the OpenGL
> programming interface in order to create 3D graphics programs. Of
> course today, OpenGL is only one of the 3D graphics standards and
> there are others like DirectX. However, the basic concepts in all of
> these standards are similar and that's fundamentally what we are
> trying to get at in this course. So the current lecture deals with an
> introduction to OpenGL and some simple demo code. So you have for
> homework 0 compiled a simple demo program, and all of you have run
> that. In this sequence of lectures we'll show a much simpler version
> of that which just outputs of plane. So here is my program and
> essentially I've just got two planes, one on top of the other. We'll
> have this plane moving in and out. This sequence of lectures is also
> somewhat different because we are going to talk about actual code and
> I'm going to show you the actual code that's used in this program, and
> we may even write actual code during the course of the lecture. The
> current lecture deals with very basic OpenGL setup, what you need to
> do to get a simple plane on the screen. The next two lectures build on
> that to consider more interesting aspects such as lighting, which is
> very relevant for homework 2. What is OpenGL? It is a graphics
> programming interface, API or abstract programming interface. The idea
> is that the internal hardware of your graphics card is dependent on
> the specific graphics card, but we want a layer of abstraction between
> what the user thinks about and the low level operations that are
> actually performed. Furthermore, OpenGL performs a uniform instruction
> set and is a portable library. It can fit in many places. The way
> you're going to be using it to in this course as a layer between the
> programmer and the graphics system. But you could also imagine the
> higher-level API built on OpenGL. An example of that that you are
> using is just GLUT. GLM is a sequence of macros that's built on
> OpenGL. So, the question is why do we need OpenGL or why do we need an
> API at all? When I was much younger and playing around on home
> computers, you did graphics in 2D by directly turning pixels on and
> off. The maximum you went was drawing circles and rectangles. So why
> do we need APIs for 3D graphics? And the idea is that there are many
> fundamental concepts in 3D graphics. Such as even what you've
> considered in the previous lectures of taking a point, transforming
> it, displaying it on the scene. And in many ways, this is similar to
> the way we write high level programs. In the olden days, of course,
> people programmed directly in machine code or in assembly language.
> But nowadays, we have higher level languages to encapsulate common
> operations, make things much easier to understand, make things
> portable. And essentially, that's what OpenGL is. It's a high level
> language for 3D computer graphics. The history of OpenGL. It was
> introduced at this point 20 years ago by Silicon Graphics which was at
> that time, the leading company in 3D graphics. Today, it's maintained
> by a consortium known as The Khronos Group that includes all of the
> major 3D graphics vendors. It's the original precursor to other API
> such as DirectX, WebGL, Java 3D, and OpenGL in its various forms
> continues to be very important. So here is the programmer's view of
> things. It can, as I said, be used in 2 different ways. So in this
> simple case, this is the application and then that goes to the OpenGL
> programming interface. You might also imagine a graphics package
> sitting between OpenGL and the application. Now once it comes here, it
> controls hardware and software such as in the graphics card, and it
> controls output and input devices This is what the OpenGL rendering
> pipeline looks like and I'll just step through the very aspects of
> this. We start with the vertices, and so I've shown examples of a
> couple of triangles. And they are vertices for those triangles. These
> vertices go into a geometry processing unit where you have primitive
> operations that operate on the geometry. This is a stage that is
> programmable in modern graphics processing units, and is something
> which is known as the vertex shader. We also can perform operations on
> images, and one of the things OpenGL is good at is it has both the
> capability to operate on geometry as well as on images. And this is
> what is known as the pixel operations. After you've done this, they
> come together in terms of texture memory, and texturing is a way in
> which you can place a texture of something like this wood grain onto
> your scene. But let's talk more about the main pipeline on the top.
> And so here, you have the geometry primitive operations, and they
> operate on the vertices. But once you've got the vertices on the
> screen, you still need to decide which pixels they correspond to. And
> that's an operation known as scan conversion or rasterization. And
> essentially OpenGL is a scan converter rasterizer. If this course were
> being taught 10 or 20 years ago, one of your crucial assignments would
> be to write a rasterizer, but nowadays it's a basic component of the
> OpenGL hardware and so we can consider more interesting concepts in
> this course. Today, essentially that's all that OpenGL does. Almost
> all of the other aspects of OpenGL are programmable, but at one time
> it controlled the entire pipeline. So, once you've rasterized and
> decided which pixels are affected, then you can go through a number of
> fragment operations. And this is again a stage that's programmable in
> modern graphics processing units. And finally you write it to the
> screen, which is known as a frame buffer. Graphics hardware has
> undergone a major renaissance in the last 10 years, where the fixed
> function pipeline, where the stages had a fixed functionality
> controlled by few parameters, has been replaced by programmable
> shaders that you will be using in the course, and that enable you to
> essentially write arbitrary programs that are executed to all pixels
> and all vertices. Since 2003, we can write vertex and pixel shaders.
> And essentially, the fixed function pipeline that was there earlier is
> a special type of shader, which is the fixed shader. So this is much
> like writing C programs. We'll be writing examples in this course. You
> can also read up on the orange book. The performance is much higher
> than CPU, even when used for non graphics applications. And that is an
> interesting idea. So one of the trends that the GPUs have spawned is
> this notion of GPGPU, or general purpose graphics programming unit,
> where you use the parallel nature that they operate on streams of
> vertices or streams of pixels, to develop a stream programming
> approach to many problems which need not have anything to do with
> graphics. And that parallelism is very important, it's in fact
> influencing in many ways the parallelism in modern CPU architectures.
> The remaining segments of this lecture we'll consider a number of
> topics. We have talked about the basic idea about OpenGL. The next
> segment will consider basic setup and buffers, matrix modes. Then we
> will talk about window system interactions and how to interact with
> your windowing system and operating system and finally we discuss the
> basic drawing of OpenGL primitives and how you initialize shaders.


---

Unit 2   Lecture 6: OpenGL 1   L6V2: OPENGL1: BUFFERS AND MATRICES

L6V2: OPENGL1: BUFFERS AND MATRICES

L6V2: OpenGL1: Buffers and Matrices


