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


https://youtu.be/PTU05lo1M9o

> We are going to consider the basic setup and the buffers. What is a
> buffer? As well as basic matrix operations that you already saw for
> transformations. So, the first question is what is a buffer? In OpenGL
> see, these are some common types of buffer. First, the color buffer.
> And you can have a front buffer, a back buffer, left and right. Left
> and right is for stereo. We don't need to consider it too much in this
> course. Front and back is interesting because you only see the front
> buffer, but there is a technique known as double buffering that draws
> into the back buffer and then swaps them. There is also a depth buffer
> to hold the z values, an accumulation buffer to add up contributions
> from many images, and things like a stencil buffer. Any drawing that
> you do writes to some buffer, and that's why these are very important
> concepts in OpenGL. Most commonly you would write to the front buffer
> or the back buffer if you were doing double buffering. And you would
> also modify the depth, because you will use the technique known as
> Z-buffering to only draw the objects that are directly visible, and
> eliminate objects that lie behind them. OpenGL does not include any
> specific aspects of window system interactions. And this is done
> mostly for portability. But we can use alternatives, such as GLUT,
> which you will be using. And there are a number of other tool kits
> (Motif, GLX, Tcl/Tk). And all of these implement callbacks, that is
> functions the user registers to handle events such as a mouse moving
> or a key press. And if you have looked at the source code for homework
> 0, you see the way these things are handled. So this is the basic
> setup code. And again we're showing a lot of code on these slides. You
> are welcome to use any of it if you think it's helpful in your
> assignments. So here is the main function. And this code is really
> just from the homework 0 program. And I'm going to build that program
> out slowly. So here's my main function. I initialized GLUT. And then I
> come to this quantity here. So glutInitDisplayMode. And what I'm going
> to do is request the single buffer, so I can have also double
> buffering, but this is single buffer, and I'm requesting the color
> buffer, RGB, red green and blue. I set the window size, window
> position, create the window and then this is something that happens
> just in order to setup my program, we won't go into it in detail, it's
> required to get all the functions to work correctly, glewInit, and
> finally I call my own initialization. In the next screen, I'm going to
> show you that I register callbacks for various keyboard and mouse
> actions. So, this was the earlier part of the main function. And now
> see, the display function is some function known as display. reshape,
> if I try to reshape my window, if I try to press the keyboard, I press
> the mouse, and also if I drag the mouse. After this you go to
> glutMainLoop, and all this does is, it waits for events, such as
> moving the mouse, pressing the keyboard, and then it calls the user
> function. The next part is to discuss matrix modes and we will talk
> about viewing in OpenGL. Of course you already have a reasonable idea
> of how this works in previous two lectures. We did consider gluLookAt
> and gluPerspective, and we did derive the matrices for them, in fact
> you will be implementing this in homework 1. Viewing in OpenGL we've
> already discussed consists of two parts. The first is to position the
> object and also to position the camera appropriately. This is known as
> the ModelView transformation matrix, and so Model and View. So View is
> for the camera, Model is for the model transformation. The final step
> is to project the 3D world onto the image, and that is known as the
> projection transformation matrix. We'll talk both about modern OpenGL,
> and we'll talk a little bit about old style OpenGL. In some cases, the
> concepts are actually easier to understand in old style OpenGL. But
> modern OpenGL responds to the notion that, today, you have
> programmable shaders. And there are therefore better ways of doing
> certain things. Now, I should mention that the old style OpenGL, for
> the most part, is still supported. There's a lot of legacy code out
> there. And in terms of doing your homeworks, you're welcome to use
> either, within the limits described in the homework assignment. So in
> older OpenGL there are two matrix stacks, the GL_MODELVIEW_MATRIX and
> the GL_PROJECTION_MATRIX. And what you do is, push and pop matrices
> onto these stacks. In new style OpenGL, you use the C++ standard
> template libraries to make stacks as needed, and in fact for homework
> 2 we do require that you use those. So in order to actually learn the
> material and homework 2, you can't just use the transformation stacks
> and old style OpenGL. This is in C++. For those of you who are not
> familiar, stack is a primitive type in C++ in the template library and
> this is a template, so I'm saying it's a stack of mat4. mat4 is
> defined in GLM, which is the auxiliary library provided, which is 4x4
> matrices, and I defined modelview. So that's just a stack of
> modelview. And I can say modelview push the matrix on to the stack, in
> this case, the identity, and can pop from it, and so on. Now of
> course, old style OpenGL supported a lot of things that are removed in
> new OpenGL. So what do you do if you want to use them? The modern way
> to handle this is to use an auxiliary library, the GLmath library,
> which supports many of the deprecated commands in a modern way. And it
> includes the mat4 type, for example. OpenGL's camera is always at the
> origin, and it points in the -z direction. We've already seen this
> when we considered transformations. Therefore, transformations
> conceptually in OpenGL move objects relative to the camera. Of course,
> they are exactly equivalent, whether you think of the camera itself
> moving or whether you think of objects moving. We have in fact
> considered both viewpoints. So we have considered the viewpoint of the
> camera at a given location and how do you transform objects into that
> reference frame. But the 4x4 matrix we derived is exactly what's
> needed for the OpenGL convention or fixing the camera and moving
> objects. In old style OpenGL, matrices are column-major. This is a
> source of great confusion because the standard mathematical way of
> writing them is row-major. And furthermore, they right multiply on the
> top of the stack. So if you say I put another matrix on the stack,
> then it'll be the first transform applied. So the last transform in
> the code is the first transform actually applied. And there is some
> confusion in GLM because it stores things in row major order but then
> it seeks to support OpenGL, and so you should really be sure you are
> doing the right thing when you use OpenGL and GLM. So here is our
> basic initialization code for viewing, and I will go over each of the
> individual steps. So we've included GLUT, we've included the standard
> library. And these are just initializations of variables. So here is
> the clear color, so I just wanted it to be black. And these colors are
> red, green, blue and then there is an alpha channel and that's not
> relevant at this stage but it's used for compositing and for
> transparency. So, now I'm going to the matrix mode, GL_PROJECTION, and
> I'm setting it to the identity. Then I go to the matrix mode
> ModelView, load the identity, and then give my gluLookAt command.
> Remember that gluLookAt is first the eye. So 0, -2 and +2. So remember
> that eyeloc is equal to 2. Then what am I looking at? In this case,
> the origin. And then the up direction. So I set it to (0, 1, 1). Note
> that it's not normalized, but OpenGL will automatically normalize it
> and create a coordinate frame, as we discussed in gluLookAt. We will
> continue discussing the initialization later, and we'll discuss the
> geometry and shader setup that you will need.


---

#### Unit 2   Lecture 6: OpenGL 1   L6V3: OPENGL 1: WINDOW SYSTEM INTERACTION AND CALLBACKS

# L6V3: OPENGL 1: WINDOW SYSTEM INTERACTION AND CALLBACKS

### L6V3: OpenGL 1: Window System Interaction and Callbacks


> We're now going to talk about how OpenGL interacts with the Window
> system, really how GLUT interacts with the system, and how we can
> define callbacks and control, for example, mouse motion. First I would
> like to mention that Window system interaction is not part of OpenGL.
> Therefore you have to use a toolkit; GLUT is the one we use. It
> defines callback functions for events. This is a very similar
> architecture to other kinds of programming environments such as X,
> Java, etc. Therefore you can define callbacks for the keyboard, for
> the mouse, for opening, initializing, re-sizing the window. If you
> just look at our main function, we had a callback for display, we had
> a callback for reshape, callback for the keyboard, for the mouse, and
> dragging the mouse. Let's first discuss the keyboard function because
> it's a basic example of what a callback function looks like. You have
> as inputs, the key, and then you also have the x and y coordinates of
> where the key was pressed, since it may behave differently at
> different locations. In our case, we do almost nothing with the
> keyboard. If you hit Escape, the ASCII code for Escape is 27, that's
> why I have said case 27, then I will exit. The reshape is another
> callback, so if I reshape the window with some width and some height.
> I set my glViewport command to that width and height. That is one
> place where we use glViewport. Look what happens next. I go to the
> projection matrix, I load it with the identify, and then I give the
> gluPerspective command, where the only thing I change is the aspect
> ratio of width to height. Let's look into that in a little bit more
> detail. First let's consider this number 30. We know that that is the
> field of view in the y direction. So it is the field of view in the y
> direction and that's the first parameter to gluLookAt. Now let's
> consider this next one which is where w and h really come into play,
> and we know that width by height (w / h), this is the aspect ratio and
> that's where they really come into play, so you are affecting the
> aspect and this ensures that the image will be filled up and the
> window will display the image with the proper proportions. The near
> plane and the far plane. Okay? So I can write that as, let me just
> write it as n and f. And that's been a brief refresher of the
> different commands, to, or the different arguments to gluPerspective.
> Note that the model view matrix is not affected because the camera
> location hasn't changed, and only the perspective matrix, or the
> projection matrix changes. Here is the mouse motion. Let me go over
> each of these steps in detail. We have the state of the mouse, the
> button that was handled, the coordinates. If the button is the left
> button of the mouse, well if the state is up, you do nothing, but if
> the state is down, you get ready to begin a drag. And look at the way
> this is handled. The old x, which is the starting point of the drag,
> is set to the current value. And what that means is that the drag is
> relative. When you stop pressing the mouse, from that point on your
> relative shift will control how the object moves. If you press the
> right button and it's down, then I just reset gluLookAt. So I will
> reset eye location to its initial value, go to the model view matrix
> and load the identity, and then reset it with my original gluLookAt.
> Note the command gluPostRedisplay. This is a very important command.
> And essentially it tells GLUT to queue up the display function as soon
> as possible. This is important because I have changed all my
> parameters, but now I need to redraw the scene. I will show you the
> demo of the mouse program. So let's look at my scene. I just have a
> plane here. I actually have one plane above it which we've not seen,
> and what I am going to do is just move my mouse. So here's the
> position, and I click left at this point in time, and I can zoom in
> and I can zoom out and that's relative to where I clicked. Now I am
> going to release the button, move to another location and click. Note
> that nothing happens when I first click. It's only when I drag that it
> zooms in, and when I drag, then it zooms out. Zoom in. Zoom out. Zoom
> in. Zoom out. So I already showed you the demo of dragging the mouse,
> and here's what the function looks like. Notice that the y location is
> now given by y minus the old value, so it's the increment. And, the
> eye location, increments, by some, function, times the Y location. I
> don't let it get less than 0. I set it back to 0. After I'm done with
> this drag, I reset the mouseoldy, so the drag is always relative to
> the previous location. Finally, I have to go and set the eye location,
> so I go to the model view matrix, load it with the identity, reset
> gluLookAt and queue the display function.


--- 

#### Unit 2   Lecture 6: OpenGL 1   L6V4: OPENGL 1: DRAWING

# L6V4: OPENGL 1: DRAWING

