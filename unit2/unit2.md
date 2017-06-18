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

> Finally we can talk about how do we actually draw anything of
> interest. So far we've set up buffers, we've set up windows, but we
> don't have any geometry to actually appear on the screen. This is what
> we are going to discuss in the current segment. OpenGL provides a
> large number of primitives, points, lines, polygons, triangles, quads,
> quad strips, triangle strips, triangle fans. The strips and fans are
> just more efficient ways of specifying primitives if you have multiple
> triangles that share vertices, you can describe them with fewer
> parameters. So in a triangle strip you have these 3, these 3 vertices
> defining a triangle, the next triangle shares two of the vertices, and
> so you need to define only one new vertex for it. So essentially you
> have one new vertex per triangle. In the triangle fan there's a
> central location and then you define the vertices around it. So, you
> can define points with GL_POINTS, we'll just talk about glBegin,
> glEnd, newer ways of specifying geometry. It's stored in homogeneous
> coordinates; you can define line segments using GL_LINES. Polygons,
> the one assumption is that these are planar convex polygons, and
> simple also. Even concave polygons are a bit hard. For more complex
> shapes, I would suggest you tessellate and use GLU, has some
> utilities. We've already talked about strips, loops, triangles, fans,
> quads, and ways in which of handling them. GLUT introduces a few
> additional primitives. And in fact, we've used the GLUT primitives in
> homework 2, so that you don't have to bother too much about
> instantiating geometry and you can focus on the lighting and shading,
> which is what homework 2 is about. So the GLUT 3D primitives are a
> cube, sphere and teapot. And indeed, these are the primitives that you
> will be using in homework 2. OpenGL drawing has gone through an
> evolution. I'll talk first about the old OpenGL way of drawing, which
> many students actually feel is easier to understand and easier to use.
> And then I'll talk about the modern way in which OpenGL drawing is
> done using vertex buffer objects. Note that both methods are currently
> supported. It remains backward compatible. However, they do encourage
> the new method, but it's not required. In old OpenGL, you have the
> client-server model. The client encloses a list of vertices between a
> glBegin and glEnd pair. Moreover, we can include normal C code, so for
> example if you want to compute the vertices on a circle, you can use
> sines and cosines. Inside are commands like glVertex3f and glColor3f.
> What is the 3f for? It's really because OpenGL is C-based, remember it
> dates back to '92. It doesn't include function overloading. So 3f
> means floating point arguments, 3 of them are input. If it were 3i, it
> will be 3 integer arguments and it defines different functions for
> each of these. One thing that people often get confused with is they
> say, "I define a vertex, I define color, vertex color". Let my just
> write this down. So I can say glVertex, and then I can define glColor
> after that. This is a common mistake, you should not do it in this
> order. So what you think is, I'll define the geometry and then I'll
> define the color and this color should be associated with this vertex.
> In fact, per OpenGL conventions, this is wrong, and what you should
> really do is define the color before you define the vertex. The reason
> for that is that old style OpenGL is really a state machine.
> Therefore, what needs to happen is that it reads the current state,
> and you need to set the state before you call the glVertex command.
> It's really an assembly line. You pass the vertices. OpenGL takes
> them, transforms them, shades them. And all of the processing is
> currently what you can program in the vertex and fragment shaders on
> the GPU. This is immediate mode, where the data you put out is
> immediately handled by OpenGL. The retained mode is where it's
> retained so it can be reused and optimized. In fact the modern OpenGL,
> the vertex buffer objects, is essentially trying to develop fast,
> efficient retained mode algorithm. Continuing on with old OpenGL, this
> is what drawing in display would be like if you wanted to draw a
> polygon. And, in fact, this is essentially the code that I used before
> I switched to more modern OpenGL to draw the plane that I've just been
> showing you in the demos. So what we say is display, clear the color
> buffer bit, and then I define the color. So I define the color red,
> and I put it at (0.5, 0.5). Incidentally, this is a useful debugging
> trick. If you just draw a plane, you may not know which vertex in your
> code is where in your screen. But if you give them each colors, it's
> very obvious, and OpenGL will interpolate the colors. And so this is a
> nice way of labeling the vertices in the scene that you are drawing.
> So this is (.5, .5), is red. Then you can go to the next one, which
> has color green and is (-.5, .5), and you go through so you have color
> blue (-.5, -.5) color white. Note that glColor always comes before the
> glVertex. Then glEnd means that within that block you are specifying
> the geometry, and flush is just a synchronization command to send the
> commands to the server, flush the queue. So all old style OpenGL
> operates on this client-server model even though in practice the
> client and server are almost always on the same computer. And so
> glFlush forces the client to send what could be a network packet, but
> it's usually just an internal synchronization. glFinish waits for the
> ACK and should be used sparingly. That's all that I have to say about
> drawing in old style OpenGL. You can specify the type of object that
> you're drawing. GL_POLYGON, GL_TRIANGLES, and so on. New OpenGL
> defines these new concepts known as vertex buffer objects that are
> more elegant and more efficient. We have included examples of them in
> the demo code we provide. At that same time, I do want to say that
> they are more complicated. If you're writing your first OpenGL
> programs, you may want to start with old style OpenGL. So here is the
> floor specification. I have just defined a number of arrays which
> contain various types of information. So here is the floor vertices,
> so I have 4 vertices, each of which includes 3 coordinates. These are
> in inhomogeneous coordinates. I have floor color for each of the three
> vertices. And again red, green, blue, white. Then I have the floor
> indices, so I want to consider 0, 1, 2, and 3, which is just one
> polygon. And then I have the floor vertices, which is a definition of
> the second object. So that's why I have called it floorverts2. So
> remember that I actually do have 2 planes, although we will be
> focusing on the first one. And similarly I have defined floor color 2
> and floor indices 2. So here is what I do to setup the vertex buffer
> objects. The number of objects is 2 in this case. The number of
> buffers per object is 3, so vertices colors and indices. Indices is
> just a pointer to the vertex. Instead of saying, draw from vertex 1 1
> 1 to 2 2 2 to 3 3 3, I just define the vertices first and then I say
> connect vertex 0 to vertex 1 to vertex 2 to make a triangle. It's a
> very standard way of doing things. So the buffers per object, list of
> buffers for the geometric data, and then you have objects, and so
> defining a number of different arrays, primitive type is the type of
> primitive, quads, polygons, and the number of elements is the number
> of geometric elements, whether they're triangles, quads, etc. Now we
> also have this buffer offset macro and this is discussed in the OpenGL
> red book. It ensures that we can offset certain number of bytes. We
> don't have to worry about it. Similarly we have the number of array
> macro, again, taken from the red book, which is just how many numbers
> does this array have. I've defined vertices, colors, elements to
> define the 3 arrays. And FLOOR and FLOOR2 for the objects on the
> scene. Here is my actual program, and I will go over it in detail.
> First I define my offset, as object times numperobj. And that's just
> because different objects are stored differently and multiplying these
> together ensures I get the correct buffer number. Thereafter, I have
> to bind the buffer. So, this is an array buffer and I have to bind it
> with the appropriate buffer. So, in this case it's vertices. So, let
> me just consider that. And so, here I'm talking about vertices. Then I
> have to define the data in the buffer, which is, size of the number of
> vertices and vertex. And GL_STATIC_DRAW is just a command which tells
> the system how to optimize things. Alright. So then I define a
> glVertexPointer into the buffer. And this is 3 variables. They're of
> floating point type. And I have my buffer offset into the buffer. And
> then I enabled the client state of the GL_VERTEX_ARRAY that enables it
> to be drawn. Okay. Then the second thing is, I bind the buffer with
> the colors, go through the same kind of analysis. Define the color
> pointer, enable the client state. The final step is, perhaps,
> interesting. So I define the GL_ELEMENT_ARRAY_BUFFER. So now that's
> not an array, it's an array of elements. So that's the indices, like
> 0, 1, 2, 3 and again defining it appropriately. I set the primitive
> type of the object to the type, so that's triangles/quads, and the
> number of elements on the object to the number of indices or the
> number of faces. And this is the command to initialize the buffers. Of
> course, this is, I realize, fairly complicated, and it's just the
> standard syntax that's used in OpenGL, and I've given you an example
> of the code so that you can build off it. Having defined the buffers,
> we also need to draw the vertex object. And once we define the data in
> the buffers, the code is actually very similar. I bind the buffer
> appropriately, and then I, and essentially that's what I need to do.
> So the only difference from the code you saw previously, is that I
> don't specify the buffer data, that's already available to me. And so
> you see colors, I am binding the buffer for the elements. Now what do
> I do inside the void display, I call drawobject for FLOOR and FLOOR2
> and notice this final command, it actually does the drawing, so it's
> glDrawElements. It takes the primitive type for the objects where they
> are triangles/quads, the number of elements and it goes to the
> appropriate buffer. So the buffer has been bound to the elements. All
> of this is essentially just standard syntax in OpenGL for drawing. It
> may be a bit confusing to understand but we've given you the sequence
> of commands so that you can build on it. Let's talk about
> initialization for drawing and shading. So I've defined a vertex
> shader, a fragment shader and a shader program. And these are
> important to the initialization. So what I first do is call this
> glGenBuffers command. And it generates a number of buffers equal to
> number per object times the number of objects. I initialize the
> objects for FLOOR and FLOOR2. And then I call the vertex shader, the
> fragment shader and the shader program. We'll be talking a little more
> about the different steps and setting up in OpenGL shader later. But
> for now, this initshaders just returns a numbers for the vertex and
> fragment shader. And the shader program essentially links them
> together. So it takes the vertex and fragment shader and makes a
> shader program. Notice that I have here file names. So let me just
> draw this, fragment shader and vertex shader. So the fragment and
> vertex shaders live in files that are the specific locations, and in
> fact they are compiled on the fly. So you don't need to recompile your
> program if you change the vertex or fragment shaders. Having shown you
> all of this code, it might be more instructive that I actually do a
> demo of changing colors. It's actually very easy, so let me bring in
> my text window where I have the code. And here I have the floor color,
> so this is red, green, blue and white. What I am going to do now is
> that I will comment this region out. So let me copy it. I am just
> showing you all the steps involved just so you get a sense that this
> is a real code that I'm going to write here. So I will go ahead and
> comment out the earlier line. And now I'm going to change the color.
> So, for example, I could make this all white. So let's make it all
> white. And if I do this I should get a completely white floor. The
> final one is already white, so let me save this file. And you may have
> a number of different compilation environments, but I'm running this
> on a Mac and you can, I'm just using make. So it runs the make file
> and notice that there are a few different definitions,
> GL_GEXT_PROTOTYPES, OSX and all of these things are of course
> specified for you in your makefile, you already have the compilation
> environment set up. So now I can run the program mytest1. And let me
> bring it in here. Notice that the plane on top is still the same, so
> that hasn't changed but the plane on the bottom is now white instead
> of being multicolored. They still have the same interactions like in
> zoom in and zoom out. I can press escape to quit since I have that in
> my keyboard routine. And if I now change back to the colors, it would
> go back to being multicolored. So let me just comment this out and
> I'll change it again. Not necessarily a very exciting demo but it is a
> first step showing that you can write these types of programs. Now you
> can see that it is in fact multicolored, the plane, because it has 4
> different colors and they are interpolated.

---

#### Unit 2   Lecture 6: OpenGL 1   L6V5: OPENGL 1: INITIALIZING SHADERS

# L6V5: OPENGL 1: INITIALIZING SHADERS

### L6V5: OpenGL 1: Initializing Shaders

https://youtu.be/R8aUykcxYjA

> The final segment in this initial sequence on OpenGL deals with
> initializing the shader. Let's go back to the OpenGL rendering
> pipeline. As you can see, there are vertices and images that both go
> through the OpenGL pipeline. Vertices are transformed by a vertex
> shader. Then you do scan conversion, generate fragments, that's where
> the geometry intersects each pixel, is called a fragment rather than a
> pixel because multiple geometric objects could intersect the pixel.
> You might have multiple fragments for a pixel because of things like
> antialiasing. Those fragments are processed by the fragment shader.
> This lecture is about how you set up the bare bones, no-op fragment
> and vortex shaders and hook them into OpenGL. So the simplified OpenGL
> pipeline, user specified vertices, vertex buffer object. For each
> vertex in parallel, OpenGL calls the user specified vertex shader,
> which transforms the vertex. In the simplest case, just does model
> view and projection matrices. For each primitive, OpenGL then
> rasterizes these transformed vertices and it generates at least one
> fragment for each pixel the corresponding vertex covers. For each
> fragment in parallel, the OpenGL calls the user specified fragment
> shader, which then goes through shading and lighting calculations.
> OpenGL, by default, handles the Z-buffer test by itself, but you can
> override it. The shader setup consists of a number of individual
> steps. So we'll discuss the shader itself later. First you have to
> create the shader, vertex and fragment shaders. Then you have to
> compile the shaders, you have to attach the shaders to a program. You
> have to link the program, and you have to use the program. And you
> have to do each of these steps. So what is a shader? It's just a
> source which is a sequence of strings. As far as the C program goes,
> it's a sequence of strings. And then, you just compile these strings
> just as you would compile a normal program. Here is the shader
> initialization code. This is my initshaders code. GLenum type is
> vertex or fragment and the file name. And this code is largely derived
> from what is recommended in the OpenGL book. So look at the different
> steps. So first you create a shader of the given type. Then you read
> the text file. That's my own command for reading the text file where
> the shader is stored. The shader, remember, as far as the program is
> concerned, is only a sequence of strings. But I've stored it in a text
> file. Okay, so you set up a new array, which is the size of the
> string, and let's ignore this. This is just to get a constant
> character so you don't complain. And it copies it in here. So then you
> define the shader's source for the given shader. It has only one
> string. You give the string, and this remaining parameter you don't
> need to use. You then compile the shader. And here is something
> interesting. From OpenGL, you can get a number of status flags. So,
> this is the status flag which tells you what the compile status is. If
> the compile status has an error, I call this function to describe the
> shader errors. And this is C++, you throw an exception. If the compile
> thing doesn't have errors, I return the number of the shader which I
> get from OpenGL. Next step is to link the shader program, and so here
> I have given the vertex shader and I have given the fragment shader. I
> create the program, I attach them to the program and then I link the
> program. Again, I get the link status, and if it's linked, I use the
> program. If it's not linked, I have to throw an exception and print
> out errors. Finally we come to what a basic shader will be, and this
> is in your directory, it's in the shaders directory, it's called nop
> because it really doesn't do much. It's almost no-op shader. Of course
> it will make it more complicated in subsequent lectures. And we have
> done it for vertex and fragment. It is written if GL shading language
> known as GLSL, which much like OpenGL itself provides a unified API in
> which to write shaders, which will later be compiled of course
> internally onto the graphics card. We have both a vertex shader and
> fragment shader and they communicate because the outputs of the vertex
> shader often inputs to the fragment shader. So, in fact, the outputs
> in vertex shader and vertices are interpolated and rasterized and
> given to the fragment shader. Version is the version of the GLSL that
> is used. I think it's currently up to 300 or 400, but I just want to
> be completely backward compatible, so I am using 120. There's also
> the, the language has been changing and so this command varying is
> technically correct in 120 and some cases I've used attribute, and
> that doesn't work on the Mac. So, just follow the skeleton code that
> you are given to know the correct command to use. In and out is
> something that they recommend more modernly, but in either way, the
> skeletons that we provide should work, and should have the right
> command. The important thing is that this says that this vec4 color is
> an output variable from the shader, which will then go into the
> fragment shader. So the main command, just like in C, it's pretty much
> code as written like in C, but you have a lot of interesting things
> you can do also. Like you can swizzle. You can have half vectors and,
> there's a lot of information that's provided if you look up the GLSL.
> So gl_Position is equal to projection matrix. So gl_Position is a
> special thing that says where the position is. Projection matrix times
> model view matrix times the vertex. And this is just the standard
> projection times model view. And the color is, again, the special
> variable GL color, which is the input color. But I have explicitly
> used this to pass it to the fragment shader, and show you how that's
> done. Here is my fragment shader. Again, this attribute you should
> probably replace with varying on the Mac. And our skeletons are
> correct. In other cases, you might want to use in and out. Essentially
> it is a no-op, where it just says, GL fragment color, again a specific
> thing which is what is the color of the fragment, is just equal to
> color. So it's just showing you the basics of how you pass an argument
> from the vertex shader to the fragment shader.


---


#### Unit 2   Lecture 7: OpenGL Shading   L7V1: OPENGL SHADING: MOTIVATION

# L7V1: OPENGL SHADING: MOTIVATION

### L7V1: OpenGL Shading: Motivation

https://youtu.be/vAn2auo1LeQ


> In this lecture we are going to study shading in OpenGL which is
> critical in order to do homework 2 and gets you excited about the way
> in which you can actually light and shade objects in a scene. In
> particular this lecture deals with lighting and will briefly explain
> the shaders that we used for the mytest3 program that you compiled for
> homework 0. We'll do this before explaining the full code base for
> mytest3, so that you have all of the material you need to get started
> on homework 2. Furthermore, we will explain all of this with reference
> to the source code; there is of course an interesting question about
> how to in a correct and physically based way, how do you do shading.
> We will not get into that in this lecture. It's an interesting topic
> that we hope to cover in a future course. As far as this lecture is
> concerned it will deal with the nuts and bolts of how do you create a
> nice smooth shaded scene. I'm showing you the demo for homework 2
> here. This is the solution. The idea is that you read a text file that
> specifies all of the geometry here. And then your program will display
> the scene with the correct shading. Notice that I still have the same
> functionality I had in homework 1. Which is that I can move about the
> scene. And the shading, you notice the highlight here that changes as
> I move the scene to different locations. Notice that you have
> highlights, both you have the red and the blue highlight on the
> teapot. You have highlights on the spheres. This lecture and homework
> 2 will tell you how to basically create a nice scene, like what we
> just saw. Let me also go back to the demo for mytest3 and as I bring
> up the demo in a moment pay attention to these different aspects.
> You'll notice that the teapot has lighting on it. It has the red and
> blue highlights that you can see. Also notice that you have diffuse
> shadings. So where you don't see the red and blue highlights the
> teapot is still lit and it's still shaded. You'll notice that the
> floor has this wood texture in it. And you'll further notice that all
> of the shading is not pasted onto the object. It actually updates as
> you move around. So here is my scene, and I can get the teapot to
> animate. So, in this case, the teapot is animating somewhat slowly, so
> you can see the motion. And here you notice that you have the blue and
> the red highlights, and as the teapot is moving those highlights are
> changing slowly; their locations are changing. You notice the texture
> on the wooden floor, and you also notice that where you don't have
> highlights on the teapot, you have this general diffuse shading. Why
> do we care about lighting? In the previous lecture on OpenGL, we just
> set up a basic scene with 2 quads. Of course you won't be very happy
> with that if you just have a quad in the scene. And lighting is
> important as shown here. So if you look at the sphere on the left,
> you'll see that it's rendered with flat shading, and there you can see
> the polygonal facets. But, it still looks somewhat interesting because
> you have that highlight on this sphere. If we were to just paint it in
> a constant color it would look like a flat disc made of paint and
> indeed the image on the screen is just a circle. So it's not any
> different from a disc. So in fact, by putting in the shading, the
> diffuse shading, also the highlights, it really gives the appearance
> of shape perception. If you've taken a computer vision course, one of
> the key cues by which we perceive shape is shading. And in fact
> there's a rich area in computer vision known as shape from shading. So
> this accurate lighting and shading is really important to convey the
> shape of the object. Furthermore, it then looks like an image that you
> can imagine in the real world. The way shading is done is also
> important. In flat shading, the entire face has a single color from 1
> vertex. And so you can think about this as being a flat plane, that
> just gets lit by the color at the left-most vertex, for example. Also,
> if you have a surface normal, that normal is assumed to be the same
> across the face. And for this reason, you do see the polygon or
> faceted appearance on the left. Whereas on the right, you are actually
> using the same geometry, but in fact you, it enables smooth shading.
> So this is something that was invented by Henri Gouraud, at the
> University of Utah. And what he does is a simple interpolation of
> shading across the vertices. Furthermore, you can interpolate the
> normal across the vertices to get specular shading to work out. We'll
> study all of these in subsequent segments. Before we go further, all
> of you are used to looking at color images. And so we have to say
> something about color. Now color is a fascinating topic and it's
> something we could spend an entire course on. But here I'm going to
> give you a very brief one slide primer on color. As humans, we are
> largely sensitive to these three primary colors: red, green and blue.
> Of course in practice we have a range of sensitivities across the
> visible spectrum but, we have standardized in computer displays for
> these three primary colors and one of the common illustrations you see
> in books is a color cube where you place red, green and blue at the
> vertices of the cube and then you can combine colors in various ways,
> and this can be drawn in fact as a Venn diagram. So let me draw this
> here, so you can imagine that this is equal to red, and then you have
> the green color here, and I draw the blue color here. Okay? So this
> area, where red and green meet, this area here, is what will be
> yellow. Whereas this area, where red and blue meet here will be
> magenta, and where green and blue meet here will be what's known as
> cyan. And then the interesting thing is what happens when all of them
> combine here, and that is white. So red plus green plus blue is equal
> to white. The intersections of red and green is yellow, blue and green
> is cyan, blue and red is magenta. These are known as the secondary
> colors. And red plus green plus blue is equal to white. For some of
> you who've been interested in paints, or even like what you get on a
> printer, these relations may seem a bit strange. That's because on a
> computer display you do colors in an additive fashion. So you add
> colors. So that means when you say red plus green you are adding red
> and green color. Whereas in paints or even in printers it's actually
> subtractive model where you have a certain base color and by then
> adding another color you actually do a subtraction and those color
> spaces are different. Now, each color channel, red green and blue is
> treated separately. That is the common assumption. Of course, in
> reality you want a full spectral color distribution. Within computer
> graphics or digital computers we just deal with 3 primaries. In
> OpenGL, one very often uses an RGBA mode, where RGB is fairly clear,
> and you typically use 8 bits per color channel. "A" stands for alpha
> or transparency. We won't get into it much here, but you can imagine
> that you want to blend one object or the other. So totally, this
> corresponds to 32 bits or 4 bytes, and in the frame buffer you will
> typically need 4 bytes for each pixel in the frame buffer. In OpenGL,
> colors are normalized from the range from 0 to 1. But of course, if
> you representing them with 8 bits, they have to range from 0 to 255 in
> terms of pixel intensities. And if you look at the image and you
> inspect it in some kind of program, typically you'll get a value from
> 0 to 255. But OpenGL tries to abstract that for the most part,
> considering colors normalized from 0 to 1. They do clamp to that
> range, so if you get a color greater than 1, it will clamp to 1, and
> if you get the color less than 0 it will clamp to 0, and only in the
> final stage are those appropriately quantized and displayed in the
> image. Let me give you a brief outline of what the rest of this
> lecture is about. First we'll talk about Gouraud and Phong shading. In
> the context of homework 2 or in the context of the OpenGL pipeline,
> those largely correspond to vertex of fragment shading. And then we'll
> talk about the types of lighting materials and shading. So we'll talk
> about point and directional light sources. We'll talk about ambient,
> diffuse, emissive and specular shading. We'll describe the fragment
> shader that was used in mytest3. And you will need a somewhat
> generalized version of this for homework 2, and we'll discuss the
> source code in the display routine. Let me first say a few words about
> vertex versus fragment shaders. You can use either of these for
> lighting and they really correspond to what you think about. The
> vertex shader operates on vertices and the colors from that are
> interpolated across the pixels or across the fragments. On the other
> hand, the fragment shader receives some variables from the vertex
> shader. So, you may for example have normals at the vertex shader that
> are interpolated and passed to the fragment shader. And the fragment
> shader then at each fragment or each pixel does the lighting
> computation. In traditional OpenGL, before the advent of shaders, all
> of lighting was handled on a per-vertex basis. So essentially using a
> fixed vertex shader, because it's cheaper. If you have fewer vertices
> than fragments then typically you want to design your scenes so you
> have a polygon occupy several pixels. Then it is just cheaper to
> compute the expensive lighting computation of the vertices and then
> use the rasterization hardware to interpolate it. So that is the basic
> idea of Gouraud or smooth shading, and we saw an example in mytest1 in
> the previous lecture. Flat shading is of course even simpler, where
> one just uses the color at a single vertex and does no interpolation
> at all, and that leads to the faceted appearance we saw earlier.
> However, in today's hardware first it's a lot cheaper to write
> fragment shaders. The performance penalty is not that large. And
> second, many times the geometry is significantly dense that the number
> of vertices is proportional to the number of pixels. And this allows
> us to do more interesting lighting calculations. So for example,
> highlights very often don't really work well with a vertex shader. You
> need to tessellate or add enough triangles to your scene so that you
> actually can represent fine highlights. But they're easy to do in
> pixel shaders or fragment shaders. So, today, it's very often just
> more convenient to write the lighting calculation in a fragment
> shader. That's what's done in mytest3, that's what you should do in
> homework 2. In this case, what you will end up doing is that you will
> get the normals at the vertices. Maybe other information, but the most
> useful thing is the normals. You will interpolate to get a normal at
> the particular pixel, and then you will shade it using the shading
> formula. This is a technique that is known as Phong shading. I will
> just highlight that. And it's named for Bui Tuong Phong who again
> invented this in the University of Utah, where a lot of the early work
> in graphics is done. The idea, let me just briefly describe it. You
> have a curved surface like this and you have a vertex here and you
> have a vertex here. You have a normal here and you have a normal here.
> You interpolate these and you get a normal here. And this is what the
> normal you use for shading. On the other hand, if you had a highlight
> here it would show up properly. On the other hand if you just
> interpolated the shading of the vertices you may say there's no
> highlight here. There's no highlight here. So there's no highlight
> here. Phong shading is different from Phong illumination. Phong
> illumination is the formula that goes in the fragment shader in order
> to produce highlights. Phong shading is an approach whereby you
> interpolate normals, and then you apply the formula to the normals. So
> it's possible to use Phong shading with a different illumination model
> such as the Torrance-Sparrow which is one of the BRDF or the
> reflection models. There are others; we'll talk about the Blinn-Phong
> model. But, it was originally proposed by Phong so that he could
> combine the Phong illumination model, but in order to get highlights,
> you also needed Phong shading, and of course it's more accurate. We'll
> talk about both of these later, in later segments, and we'll discuss
> the whole range of shading options that one typically uses in OpenGL.


---

#### Unit 2   Lecture 7: OpenGL Shading   L7V2: OPENGL SHADING: GOURAUD AND PHONG

# L7V2: OPENGL SHADING: GOURAUD AND PHONG

### L7V2: OpenGL Shading: Gouraud and Phong


> In this segment, we are going to go into detail about Gouraud and
> Phong shading. Let's first talk about Gouraud shading which is the
> standard smooth shading. Note also that is a lecture that actually
> talks about the operations that happen in rasterization. In a standard
> vertex or pixel shader you would just give the colors for I_1, I_2,
> and I_3, and after you've done that you would expect the rasterization
> hardware and OpenGL to do the interpolation. So you don't need to
> worry about the details of this for Gouraud shading. However, we are
> interested in learning for this course what actually goes on under the
> hood. So here you have three vertices, I_1, I_2, I_3, and those
> correspond to the colors here. So, we assume I_1 is the color at
> vertex 1, I_2 is the color at vertex 2, I_3 is the color at vertex 3.
> Notice that the vertical extent goes from y_1 all the way to y_3. So
> we want to find first the, to find the color of I_P, we first want to
> find the colors at I_a and I_b, and then we want to interpolate them.
> So let's first talk about the color at I_a. I_a lies between I_1 and
> I_2, so if you want to do the interpolation, we do it along the
> vertical direction. Look at the length of this region and the length
> of this region. So, the length of this region is y_1 minus y_s. The
> length here is y_s minus y_2. The total length of course is Y1 minus
> Y2. Now it's just a question of doing the standard interpolation
> formula. Which will mean that I_1, because it's further away from I1,
> it will be multiplied by the smaller quantity. So this will get I_1.
> And this quantity will multiply I_2. Indeed, that's the formula here.
> I_1 times y_s minus y_2 plus I_2 times y_1 minus y_s. And divide the
> whole thing by the total length here, which is y_1 minus y_2. That's
> the formula for I_a. We can similarly get a formula for I_b. Which is,
> will be equal to I_1 times, in this case, y_s minus y_3, and I_3 times
> y_1 minus y_s. And now you normalize by y_1 minus y_3. Once you have
> the formulae for I_a and I_b, the question is what do you get for I_p?
> And in order to consider that one needs to consider the X coordinates.
> Because one is interpolating within a scan line. So we can consider
> this as being the x of a (x_a). And we can consider this as being x of
> b (x_b). Here of course you have X of P (x_p). So the interpolation
> idea is the same. You have this length, which is x_p minus x_a, and
> you have this length which is x_b minus x_p. So I_a will be multiplied
> by x_b minus x_p and I_b will be multiplied by x_p minus x_a. Indeed
> this is what happens here. So you have I_a times x_b minus x_p, plus
> I_b, which is multiplied by x_p minus x_a. Again you normalize by x_b
> minus x_a. So it's just interpolation first in the vertical direction
> in order to get the locations for the endpoints of the scan line, and
> then interpolation along the scan line to get the, horizontally to get
> the final color of I_p. The actual implementation of this is much more
> efficient than the formulae lead you to believe. For example I can
> precompute the division by y_1 minus y_2, I can find the reciprocal of
> that, y_1 minus y_3, x_b minus x_a and moreover you see as we go from
> one scanline to the next, the multiplicative factors, they reduce to
> addition. And therefore there are very efficient algorithms that in
> fact don't involve multiplication or division at all, that just
> incrementally add quantities as you go from one scanline to the next.
> And this is a process which is generally known as scan conversion. But
> it also does the interpolation which is needed for Gouraud shading.
> Errors, we've already talked about those in the previous segment. So
> here is an extreme case where I_1 and I_2 are 0 because either the
> light is pointing backwards or the eye does not see the point. And now
> you have zeroes in both cases and you want to interpolate to make a
> highlight. Of course that is not going to happen; if you have zero in
> the two vertices the interpolation is also zero and so Gouraud can
> have problems. Moreover, the day we implemented it where we went
> vertically and then horizontally means the shading is not rotationally
> invariant, so if you were to rotate a point you would actually see the
> shading change. For all of these reasons, Gouraud shading is useful
> only when you have relatively smooth shading effects. Mostly for
> diffused shading. But prior to the advent of fragment shaders, is you
> also needed to use Gouraud shading for specular highlights. And the
> way you handled that was by tessellating or breaking the model into
> enough triangles that relative to the size of the triangles, the
> shading is still smooth. Next we consider the Phong Illumination
> Model, which is really the motivation also for the use of Phong
> shading and the use of fragment shaders. And this corresponds to a
> specular or glossy material where you have highlights. At the bottom
> I've just showed some renderings I made many years ago where you've
> taken a lighting environment or a light probe that was acquired at
> Berkeley by Paul Debevec. It's in the Grace Cathedral in San
> Francisco. And I've rendered images with many different roughness
> settings, and you'll see from left to right it starts off being a
> mirror, then it gets blurred out and eventually on the right it almost
> looks like a diffuse surface. And that, the amount of roughness
> controls the width of the highlights and your perception of how shiny
> the object is. Examples of specular, glossy materials are polished
> floors, glossy paint, white boards. Furthermore, highlights behave
> somewhat differently from plastics or dielectric materials as opposed
> to metals. So on plastics, the highlight is the color of the light
> source, not the body color of the object. And this is a very common
> thing. You can have a green ball and you can look at the highlight,
> it's still white. Because the light source is white. Metals, on the
> other hand, the highlight depends on the surface color and is
> modulated by the surface color. We don't have time to go into the
> physics of all of these effects. Hopefully that's something you can
> look up or we can cover in a future course. But these are basic
> properties of illumination and highlights, and it's also possible to
> regard them really as blurred reflections of the light source. If you
> look in the bottom panel, you can consider that the light source has
> just been blurred out as you go from left to right. So Phong
> illumination, coupled with Phong shading is the appropriate way to
> make highlights, and again it's worth noting the distinction between
> these, they are commonly used together but technically they are
> different aspects. The idea of Phong shading is simply that instead of
> interpolating the colors, what one actually does is interpolate the
> normals. So here we have the color was 0, but there is a correct
> normal at both of these locations. You interpolate the normal, and so
> you get the correct normal at the center and therefore you can
> evaluate the illumination model and get a highlight. So the entire
> lighting calculation is performed for each pixel. In old-style OpenGL
> there was no Phong shading, it was just Gouraud shading, and therefore
> you would have to break this geometry up into enough triangles that it
> did actually compute the shading at each vertex. But in modern OpenGL
> in homework 2, you just write the fragment shader, and in this way you
> can do perfect Phong shading. Let's talk about the vertex shader
> that's used in mytest3. Again you will be adapting the mytest3
> shaders. They are very good background material for the shaders you
> need to write for homework 2. So we start off with defining the
> version and again I have gone for a very old version to be backward
> compatible. Whether this should be varying or attribute or in or out
> depends on your system and use the skeletons and all of you are set up
> now. But, essentially it's saying there are these three variables:
> color, mynormal, and myvertex, that I'm actually going to pass on to
> the fragment shader. So let's see what the main routine does. This is
> a texture coordinate, so it sets the texture coordinate from what you
> get from OpenGL, that's this gl_MultiTexCoord0, that's texture
> 0. So you can have multiple textures, that's why we use the MultiTexCoord. We'll get into texture mapping later. You then set the
> gl_Position as projection matrix, modelview matrix times the vertex,
> and then this just defines standard OpenGL variables: the color, the
> normal the vertex. But I've given my own variable to illustrate that
> what OpenGL is now going to do is interpolate these values from the
> vertices and the interpolated value will be available at the fragment
> for me to write my fragment shader. The next thing we're going to talk
> about is the type of different lighting and materials. Lights: points
> and directional, and shading: ambient, diffuse, emissive, and
> specular.


---


#### Unit 2   Lecture 7: OpenGL Shading   L7V3: OPENGL SHADING: LIGHTING AND SHADING

# L7V3: OPENGL SHADING: LIGHTING AND SHADING

> We will now discuss the basics of lighting and shading. This is really
> the key part of this lecture where we discussed the different shading
> models used and we discussed different types of light sources used.
> Putting this all together, you can understand how lighting and shading
> works in computer graphics and in OpenGL and begin to start working on
> homework
> 2. The motivation for a lot of this is what happens physically in the real world, and although this lecture will discuss the concepts
> intuitively, it is also possible to formalize them based on physical
> arguments. In the real world, complex materials and lighting interact,
> so the shading you get out of an object, what it looks like, depends
> on the interaction of the illumination in the scene and the material
> properties of which that object is made. For now, we are just going to
> talk about some very basic approximations just like we did for Gouraud
> and Phong shading, similarly in lighting models, to capture the key
> effects: the overall color of an object as well as the specular
> highlights. This lecture is largely inspired by the old OpenGL fixed
> function pipeline, and largely reproduces the shading that would be
> reproduced in that pipeline. Of course, that pipeline is not
> physically based. It's a number of approximations. And of course today
> you have the ability to write arbitrary shaders. So one of the things
> to think about after this course is ways in which you could improve on
> the shading model. Potentially make it nicer, make it more physically
> based. Let's start with the types of light sources in the scene. And
> the first light source is a very simple one, it is a point light
> source. Of course, in the real world there is no such thing as a point
> light source but many practical lamps can be idealized as point
> lights. Being a point, it has a position in space and it has a
> particular color. That's all you specify, so the position is a
> 4-vector in homogeneous coordinates, and the color is again RGBA.
> Point like sources come with this attenuation or quadratic model.
> We'll describe what this is and how to set the parameters for k_c, k_l
> and k_q. First, let's consider the case when you have a point light
> source and it is emitting light. How much light will be received here
> versus here? This is given by standard inverse square fall-off in
> physics where you take this distance r and the intensity is
> proportional to 1 over r squared. This of course holds in 3
> dimensions; in flat-land it would be somewhat different. But, in
> practice in our world, this is a standard law, it's true for light,
> electromagnetic energy, it's true for gravitation. Essentially, you
> can think about the same amount of energy being on a sphere surface of
> radius r, the surface area goes as r squared, and so the energy
> decreases. So this is a very standard argument where d is the distance
> to the light source, it applies here. And it would argue that one
> should set k_q, is equal to one. And the other components equal to
> zero. However, let's consider some other types of light sources. So
> let's consider a line light, or something like this, a cylinder, a
> tube light that's emitting light. Of course, you might wonder why are
> we considering this line light source instead of point, when we said
> we are talking about point light sources? Why don't we have a separate
> primitive in OpenGL that deals with line light sources? The reason for
> that is that a point light source is easy to shape because at each
> location on the surface you just need to look up, where the point
> light is coming from. Whereas for a line you really have to add up or
> do an integral over the entire line. And so it's very common in OpenGL
> that you might draw the geometry of a tube light, but for shading
> purposes you will concentrate it as a point source at the center.
> However, the attenuation for a line source is different, and you can
> go through the mathematics. You can go through the integration. And
> essentially the intensity falls off as 1 over the radius. So if this
> is the radius, the intensity will fall off as 1 over the radius. And
> that's where this term k_l comes from, and so you would really want in
> this case to have k_l equal to 1. And of course this is assuming the
> light source itself is infinite, so the viewer is a certain distance
> away from it, which is small compared to the light source width. Of
> course, if you're far away from the light source width, it eventually
> behaves like a point light source. And so, that would argue that you
> have this linear attenuation. And in other cases such as when you have
> a light source that's far away, or we handle that separately with the
> directional source, but instead of a line supposing it's actually an
> area source: something like this, and one it's close to the light
> source. So in that case it becomes harder to compute what the
> attenuation is and very often you may just want to keep it with the
> constant attenuation. So an example of this is what is the
> illumination you get from a wall? And one of the things we talk about,
> when we talk about radiance computations is that the wall looks
> similar from the range of different distances on it. And so in cases
> like this, you want to keep the attenuation constant. In practice,
> many people when they are doing computer graphics just ignore this
> attenuation, set k_c equal to one and in fact, in our assignments
> that's what we will be doing, right? So we will be representing the
> attenuation often, as 1, 0 and 0, even though for a real point light
> source you have quadratic attenuation. And so in OpenGL we are given
> the option of using the appropriate attenuation model that is
> appropriate to your light source. Finally, you can have a directional
> source, and you can include that within the point source simply by
> setting the homogeneous coordinate equal to 0. So if W is equal to 0,
> the source is really at infinity, and that's a good model for
> something like sun or even you have a light source which is very
> distant relative to the scene. Of course, if the light source is a
> directional source, the question of distance doesn't really come into
> play, and there should be no attenuation. In fact, the k_l and k_q
> term should be equal to 0. That's as far as the lighting is concerned;
> the next thing we need to talk about is the material properties. That
> is, how does a surface reflect light? For that we need to know the
> surface normals. So, so far we've talked and we have had one brief
> segment in transforming normals, but mostly you consider the points or
> geometry of the surface and you are moving them around to different
> locations. However, for lighting calculations it's absolutely critical
> that you know the surface orientation or the surface normal, and that
> affects the diffuse reflection, the specular reflection; it affects
> the reflective direction of the light source, you often want to find
> the reflective direction. The standard way of doing that is to specify
> the normal at each vertex and then interpolate it to each fragment. In
> some cases, for procedural models, you might have an analytic formula
> for the normal at each point, such as on the sphere. For objects such
> as teapots, spheres, et cetera, that you specify with GLUT, GLUT does
> it automatically for you. And so you might wonder how the teapot in
> all of my assignments actually has normals correctly for lighting, the
> answer is GLUT does it for you. For parametric surfaces, you can do it
> manually. And, in fact, there are some GLUT evaluators to do it for
> spline curves. For more complex shapes, there's actually an
> interesting trick in which you can average the face normals to get a
> vertex normal. And I'll show it to you in a moment. So let's assume
> you have a surface. Something like this. You have triangle 1. You have
> triangle
> 2. Now I want to get the normal at some vertex, let's say this vertex, and so I can complete that I have a few more triangles, let's say, so
> I want the normal here. What I do is I consider the normals at these
> locations and these are what are known as face normals. I average all
> of them together and you can use weighted average in order to get what
> is known as the vertex normal here. Then to get a normal in the
> interior I interpolate the vertex normals and so that's the standard
> technique of averaging the face normals for more complex shapes. Let's
> talk about the different shading modes. There are 4 basic things that
> we will consider: ambient, diffuse, specular, and emissive. Let's
> first consider the emissive term. Emission really corresponds to
> things like sunlight, things like light sources. And it really
> corresponds to emission from them only when you are looking directly
> at the light source, so not when you are looking at its reflection on
> something else. The reason for that is, if you look directly at the
> light source, even if there is no light from elsewhere falling on the
> source it is going to emit light in your direction. In OpenGL, there
> is a little bit of a gotcha that to actually see a light source it's
> not enough to create it, you must create geometry. So only geometry is
> what you see. Geometry is lit by light sources, but you don't see the
> light sources, you don't see the camera. So what I will do is I will
> create a rectangle. I mean, it's not a point because I have to see it
> for the light source. And I will give it an emissive property, let's
> say of white, so that it always appears white. That's a very common
> way to set things up. This is not relevant for surfaces that are not
> emitting light. The second thing is the ambient term, and the
> intuition there is that even if there's no light falling directly on
> the surface, there is light that's bouncing about in a room and gives
> it a general diffused or ambient feeling. So if you go into a room,
> this would be light cast typically by large light sources. Light
> that's bouncing off the wall, and so on. It's really a hack, because
> it is possible to simulate the exact distribution of light in a scene.
> This is a very rich research area in computer graphics rendering known
> as global illumination. We'll have one lecture at the end of this
> course talking about a development there known as the rendering
> equation. But, ambient illumination is a simple hack which says like
> this bouncing around the scene many times. Eventually its distribution
> is approximately uniform coming equally from all directions. So let's
> just give the scene a global constant, and the advantage of that also
> is that I will actually be able to see my computer graphics image. I
> never had black pixels. And so you just give an ambient intensity to
> the whole scene. Typically this is very low, something like 0.1 or
> 0.2. The next aspect is the diffuse term, which corresponds to rough, matte surfaces. So something like the walls, which are rough and
> matte. Something like the floor if it's not polished, faces are to a
> certain extent matte of course they have much more interesting
> reflectance properties, and this is something which technically we
> refer to as Lambertian surfaces in computer graphics, after Lambert.
> The idea is that light reflects equally in all directions. Of course,
> in practice no surface will reflect light equally in all directions.
> The closest to this is a material known as Spectralon, but even it has
> a falloff. However, it's a good idealized model in computer graphics
> that light hits a surface and then is equally reflected in all
> directions, so the surface is not smooth and polished like a mirror,
> it's a rough surface and therefore the reflection comes about in any
> direction equally. One of the key aspects of this is the cosine
> falloffs, so N dot L is just the cosine of this angle, so if you let
> this be the incident angle, this is just equal to cosine of theta in
> (theta_i). And in fact, we have to technically take a max of this and
> 0, because you don't get light from below the surface. And this is
> because you see that the light is coming in here, so it's really
> incident in a plane here. Whereas the light that's flowing normal to
> the surface is attenuated by this cosine factor. It's very important.
> It's what gives rise to season, because the sun's light is at an
> oblique angle in the winter; it's at a more normal angle in the
> summer. And we can write down the formula like this, so you sum over
> all of the light sources in the scene. You look at the intensity of
> the light source times the diffuse component of the material, times
> the attenuation for that light source, times the max of this cosine
> term or L dot N and 0. That's what the diffuse, or the Lambertian term
> is. Next, we come to specular reflections. We've already had a lot of
> talk about the Phong illumination and shading models. The specular
> reflections corresponds to glossy objects. We've said glossy paints,
> white boards, things like that. And even if you look at typical
> plastics or metals, you will have some reflection. The idea is light
> reflects in the mirror direction, so all of you in school have studied
> this law of light reflection, the incident and reflective directions,
> and the normal lie in the same plane, and the angle of incidence is
> equal to the angle of reflection. So I can write, this is the incident
> angle. This is the reflected angle. So let's say theta incident
> (theta_i), theta reflected (theta_r), and they have to be equal. But
> the eye is not actually the reflected direction. So it's really the
> rough reflection. If it were a smooth mirror you would get intensity
> only here and no intensity here. And so you can see that how far off
> angle the eye is will actually affect the amount of light that's
> reflected. So here is the reflection lobe. You can see that light is
> reflected mainly in the mirror direction, but there is some intensity
> that goes towards the eye. Let me repeat my slide about the Phong
> Illumination Model which covers specular or glossy materials. And
> really you can be considered to be blurred reflections of the light
> source, if you increased the roughness, you get a greater blur in
> terms of the reflection of light source. So let's go back and talk
> about Phong Illumination. Despite its long history, this was first
> proposed in the mid-1970s, and even though we now know that there are
> more accurate, physically based ways of doing reflection, it's still a
> very commonly used model. And Phong's idea was generally that he
> wanted a simple way to handle view-dependent highlights, not
> necessarily physically based. And so he said, where taking the dot
> product for diffused surfaces, why don't we take a dot product for
> specular surfaces. But instead of taking the normal in the lighting
> direction, we'll take the eye and the reflection of the lighting
> direction about the normal. And furthermore, we'll raise the cosine to
> some power, so you can control how shiny the surface is, how white the
> highlight is. There is an alternative form which just says, takes the
> half angle between the light source and the viewer, and take the dot
> product of that with the normal. So, then it's much closer to standard
> diffuse illumination, which is the dot product of light and normal,
> this is dot product of the half angle and normal, and again you can
> raise it to some power. That's something which is known as the
> Blinn-Phong model and actually for physical surfaces, the half-angle
> form is more accurate. It's the form in standard OpenGL and largely,
> what I ask you to implement. Let first consider the standard Phong
> formula, not the Blinn-Phong form, where you're considering the
> reflection of the light direction about the normal, that is the angles
> are the same and it's in a plane. That's why I can draw this diagram
> on a plane. And now I am looking at really, the angle between the
> reflected direction and the eye. This is between the reflected
> direction and the eye. And that angle, that cosine I am going to now
> raise to some power. Okay. So the question is, I just need to find the
> mathematical formula for the reflected direction. And it's relatively
> easy to do it, although the formula is somewhat complex. So we first
> look at the lighting direction. And I'm going to break this into the
> horizontal and the vertical components, so the vertical component is
> along the direction of the normal, the horizontal component is going
> along the surface. Now the horizontal component doesn't actually
> change for the reflection, but the vertical component, the direction,
> is changed and that's essentially what a reflection is. So you can
> take the original lighting which includes the parallel and the
> perpendicular component and what we want to do is flip this component
> along the normal. So you consider the component along the normal and
> you take twice that in order to flip it and you subtract. So
> essentially what we have is we have the lighting, then what you want
> to do is subtract out this component, so that will be the dot product
> of the lighting and the normal along the direction of the normal
> assuming all of these things are unit vectors. And you want to have a
> factor of 2 in there. So, I've just inverted the signs in order to
> make this work out and get the correct sign. But essentially that's
> what you have. You have 2 of L dot N times N, because that corresponds
> to the reflection, and then you subtract out the lighting. An
> alternative form is the half-angle form, which is the Blinn-Phong
> formula. And that's after Jim Blinn, who was one of the pioneers in
> computer graphics. Just tweak this formula a little bit, and there you
> just take the lighting and the reflected direction. You take
> half-angle between them, so you can look at H. If these were scalars
> would just be L plus R divided by 2. In our case, we can write it as L
> plus R, and you can normalize by the norm of L plus R. So what is the
> final specular reflection formula? You have some intensity for the
> light i, times the specular coefficient of the material, times the
> attenuation, times again max of N dot H, 0. Just as you had max of N
> dot L, 0, but there is this additional shininess term which controls
> how sharp the lobe is. So if shininess is very large, it's
> concentrated about the half angle direction and the mirror direction.
> If shininess is 0, then it essentially is very similar to the
> Lambertian case, except using the half angle instead of the lighting
> direction for the cosine. Okay. So let's do one example of this. Let's
> go through the mytest3 example. And here is my program. Okay. Now,
> what I want to do is change the intensity. So, let's look at this, and
> let me bring in my, editor. So, first of all I am going to make the
> teapot move a little bit faster, so I'll change this to .005. And then
> I want to change the intensity in the highlight, so right now the
> exponent is 100. Let's make the exponent equal to 10. Okay? So
> remember how the highlight looked like earlier. I'm going to show you
> writing actual code. So I come here and I say make mytest3. And it
> goes through the compilation and eventually it will make the program.
> So now all I need to do is run it. And you notice that the highlights
> are much larger. So let me make it the same size as the earlier, this
> one. And you notice that if you compare the highlights on this teapot
> here, which was my original program, to the highlights here, you'll
> see that the highlights have now become much larger. And of course, my
> teapot is moving somewhat more quickly because I made it move. I
> changed the increment. And so if I made the highlight back to 100 then
> I would get this. So this is with 10, this is with 100. And in this
> way you can shape the way in which the highlights look. In the next
> segment, we'll be talking about the fragment shaders, and ways in
> which you will actually implement this in OpenGL.


---


#### Unit 2   Lecture 7: OpenGL Shading   L7V3: OPENGL SHADING: LIGHTING AND SHADING

# L7V3: OPENGL SHADING: LIGHTING AND SHADING


> We will now discuss the basics of lighting and shading. This is really
> the key part of this lecture where we discussed the different shading
> models used and we discussed different types of light sources used.
> Putting this all together, you can understand how lighting and shading
> works in computer graphics and in OpenGL and begin to start working on
> homework
> 2. The motivation for a lot of this is what happens physically in the real world, and although this lecture will discuss the concepts
> intuitively, it is also possible to formalize them based on physical
> arguments. In the real world, complex materials and lighting interact,
> so the shading you get out of an object, what it looks like, depends
> on the interaction of the illumination in the scene and the material
> properties of which that object is made. For now, we are just going to
> talk about some very basic approximations just like we did for Gouraud
> and Phong shading, similarly in lighting models, to capture the key
> effects: the overall color of an object as well as the specular
> highlights. This lecture is largely inspired by the old OpenGL fixed
> function pipeline, and largely reproduces the shading that would be
> reproduced in that pipeline. Of course, that pipeline is not
> physically based. It's a number of approximations. And of course today
> you have the ability to write arbitrary shaders. So one of the things
> to think about after this course is ways in which you could improve on
> the shading model. Potentially make it nicer, make it more physically
> based. Let's start with the types of light sources in the scene. And
> the first light source is a very simple one, it is a point light
> source. Of course, in the real world there is no such thing as a point
> light source but many practical lamps can be idealized as point
> lights. Being a point, it has a position in space and it has a
> particular color. That's all you specify, so the position is a
> 4-vector in homogeneous coordinates, and the color is again RGBA.
> Point like sources come with this attenuation or quadratic model.
> We'll describe what this is and how to set the parameters for k_c, k_l
> and k_q. First, let's consider the case when you have a point light
> source and it is emitting light. How much light will be received here
> versus here? This is given by standard inverse square fall-off in
> physics where you take this distance r and the intensity is
> proportional to 1 over r squared. This of course holds in 3
> dimensions; in flat-land it would be somewhat different. But, in
> practice in our world, this is a standard law, it's true for light,
> electromagnetic energy, it's true for gravitation. Essentially, you
> can think about the same amount of energy being on a sphere surface of
> radius r, the surface area goes as r squared, and so the energy
> decreases. So this is a very standard argument where d is the distance
> to the light source, it applies here. And it would argue that one
> should set k_q, is equal to one. And the other components equal to
> zero. However, let's consider some other types of light sources. So
> let's consider a line light, or something like this, a cylinder, a
> tube light that's emitting light. Of course, you might wonder why are
> we considering this line light source instead of point, when we said
> we are talking about point light sources? Why don't we have a separate
> primitive in OpenGL that deals with line light sources? The reason for
> that is that a point light source is easy to shape because at each
> location on the surface you just need to look up, where the point
> light is coming from. Whereas for a line you really have to add up or
> do an integral over the entire line. And so it's very common in OpenGL
> that you might draw the geometry of a tube light, but for shading
> purposes you will concentrate it as a point source at the center.
> However, the attenuation for a line source is different, and you can
> go through the mathematics. You can go through the integration. And
> essentially the intensity falls off as 1 over the radius. So if this
> is the radius, the intensity will fall off as 1 over the radius. And
> that's where this term k_l comes from, and so you would really want in
> this case to have k_l equal to 1. And of course this is assuming the
> light source itself is infinite, so the viewer is a certain distance
> away from it, which is small compared to the light source width. Of
> course, if you're far away from the light source width, it eventually
> behaves like a point light source. And so, that would argue that you
> have this linear attenuation. And in other cases such as when you have
> a light source that's far away, or we handle that separately with the
> directional source, but instead of a line supposing it's actually an
> area source: something like this, and one it's close to the light
> source. So in that case it becomes harder to compute what the
> attenuation is and very often you may just want to keep it with the
> constant attenuation. So an example of this is what is the
> illumination you get from a wall? And one of the things we talk about,
> when we talk about radiance computations is that the wall looks
> similar from the range of different distances on it. And so in cases
> like this, you want to keep the attenuation constant. In practice,
> many people when they are doing computer graphics just ignore this
> attenuation, set k_c equal to one and in fact, in our assignments
> that's what we will be doing, right? So we will be representing the
> attenuation often, as 1, 0 and 0, even though for a real point light
> source you have quadratic attenuation. And so in OpenGL we are given
> the option of using the appropriate attenuation model that is
> appropriate to your light source. Finally, you can have a directional
> source, and you can include that within the point source simply by
> setting the homogeneous coordinate equal to 0. So if W is equal to 0,
> the source is really at infinity, and that's a good model for
> something like sun or even you have a light source which is very
> distant relative to the scene. Of course, if the light source is a
> directional source, the question of distance doesn't really come into
> play, and there should be no attenuation. In fact, the k_l and k_q
> term should be equal to 0. That's as far as the lighting is concerned;
> the next thing we need to talk about is the material properties. That
> is, how does a surface reflect light? For that we need to know the
> surface normals. So, so far we've talked and we have had one brief
> segment in transforming normals, but mostly you consider the points or
> geometry of the surface and you are moving them around to different
> locations. However, for lighting calculations it's absolutely critical
> that you know the surface orientation or the surface normal, and that
> affects the diffuse reflection, the specular reflection; it affects
> the reflective direction of the light source, you often want to find
> the reflective direction. The standard way of doing that is to specify
> the normal at each vertex and then interpolate it to each fragment. In
> some cases, for procedural models, you might have an analytic formula
> for the normal at each point, such as on the sphere. For objects such
> as teapots, spheres, et cetera, that you specify with GLUT, GLUT does
> it automatically for you. And so you might wonder how the teapot in
> all of my assignments actually has normals correctly for lighting, the
> answer is GLUT does it for you. For parametric surfaces, you can do it
> manually. And, in fact, there are some GLUT evaluators to do it for
> spline curves. For more complex shapes, there's actually an
> interesting trick in which you can average the face normals to get a
> vertex normal. And I'll show it to you in a moment. So let's assume
> you have a surface. Something like this. You have triangle 1. You have
> triangle
> 2. Now I want to get the normal at some vertex, let's say this vertex, and so I can complete that I have a few more triangles, let's say, so
> I want the normal here. What I do is I consider the normals at these
> locations and these are what are known as face normals. I average all
> of them together and you can use weighted average in order to get what
> is known as the vertex normal here. Then to get a normal in the
> interior I interpolate the vertex normals and so that's the standard
> technique of averaging the face normals for more complex shapes. Let's
> talk about the different shading modes. There are 4 basic things that
> we will consider: ambient, diffuse, specular, and emissive. Let's
> first consider the emissive term. Emission really corresponds to
> things like sunlight, things like light sources. And it really
> corresponds to emission from them only when you are looking directly
> at the light source, so not when you are looking at its reflection on
> something else. The reason for that is, if you look directly at the
> light source, even if there is no light from elsewhere falling on the
> source it is going to emit light in your direction. In OpenGL, there
> is a little bit of a gotcha that to actually see a light source it's
> not enough to create it, you must create geometry. So only geometry is
> what you see. Geometry is lit by light sources, but you don't see the
> light sources, you don't see the camera. So what I will do is I will
> create a rectangle. I mean, it's not a point because I have to see it
> for the light source. And I will give it an emissive property, let's
> say of white, so that it always appears white. That's a very common
> way to set things up. This is not relevant for surfaces that are not
> emitting light. The second thing is the ambient term, and the
> intuition there is that even if there's no light falling directly on
> the surface, there is light that's bouncing about in a room and gives
> it a general diffused or ambient feeling. So if you go into a room,
> this would be light cast typically by large light sources. Light
> that's bouncing off the wall, and so on. It's really a hack, because
> it is possible to simulate the exact distribution of light in a scene.
> This is a very rich research area in computer graphics rendering known
> as global illumination. We'll have one lecture at the end of this
> course talking about a development there known as the rendering
> equation. But, ambient illumination is a simple hack which says like
> this bouncing around the scene many times. Eventually its distribution
> is approximately uniform coming equally from all directions. So let's
> just give the scene a global constant, and the advantage of that also
> is that I will actually be able to see my computer graphics image. I
> never had black pixels. And so you just give an ambient intensity to
> the whole scene. Typically this is very low, something like 0.1 or
> 0.2. The next aspect is the diffuse term, which corresponds to rough, matte surfaces. So something like the walls, which are rough and
> matte. Something like the floor if it's not polished, faces are to a
> certain extent matte of course they have much more interesting
> reflectance properties, and this is something which technically we
> refer to as Lambertian surfaces in computer graphics, after Lambert.
> The idea is that light reflects equally in all directions. Of course,
> in practice no surface will reflect light equally in all directions.
> The closest to this is a material known as Spectralon, but even it has
> a falloff. However, it's a good idealized model in computer graphics
> that light hits a surface and then is equally reflected in all
> directions, so the surface is not smooth and polished like a mirror,
> it's a rough surface and therefore the reflection comes about in any
> direction equally. One of the key aspects of this is the cosine
> falloffs, so N dot L is just the cosine of this angle, so if you let
> this be the incident angle, this is just equal to cosine of theta in
> (theta_i). And in fact, we have to technically take a max of this and
> 0, because you don't get light from below the surface. And this is
> because you see that the light is coming in here, so it's really
> incident in a plane here. Whereas the light that's flowing normal to
> the surface is attenuated by this cosine factor. It's very important.
> It's what gives rise to season, because the sun's light is at an
> oblique angle in the winter; it's at a more normal angle in the
> summer. And we can write down the formula like this, so you sum over
> all of the light sources in the scene. You look at the intensity of
> the light source times the diffuse component of the material, times
> the attenuation for that light source, times the max of this cosine
> term or L dot N and 0. That's what the diffuse, or the Lambertian term
> is. Next, we come to specular reflections. We've already had a lot of
> talk about the Phong illumination and shading models. The specular
> reflections corresponds to glossy objects. We've said glossy paints,
> white boards, things like that. And even if you look at typical
> plastics or metals, you will have some reflection. The idea is light
> reflects in the mirror direction, so all of you in school have studied
> this law of light reflection, the incident and reflective directions,
> and the normal lie in the same plane, and the angle of incidence is
> equal to the angle of reflection. So I can write, this is the incident
> angle. This is the reflected angle. So let's say theta incident
> (theta_i), theta reflected (theta_r), and they have to be equal. But
> the eye is not actually the reflected direction. So it's really the
> rough reflection. If it were a smooth mirror you would get intensity
> only here and no intensity here. And so you can see that how far off
> angle the eye is will actually affect the amount of light that's
> reflected. So here is the reflection lobe. You can see that light is
> reflected mainly in the mirror direction, but there is some intensity
> that goes towards the eye. Let me repeat my slide about the Phong
> Illumination Model which covers specular or glossy materials. And
> really you can be considered to be blurred reflections of the light
> source, if you increased the roughness, you get a greater blur in
> terms of the reflection of light source. So let's go back and talk
> about Phong Illumination. Despite its long history, this was first
> proposed in the mid-1970s, and even though we now know that there are
> more accurate, physically based ways of doing reflection, it's still a
> very commonly used model. And Phong's idea was generally that he
> wanted a simple way to handle view-dependent highlights, not
> necessarily physically based. And so he said, where taking the dot
> product for diffused surfaces, why don't we take a dot product for
> specular surfaces. But instead of taking the normal in the lighting
> direction, we'll take the eye and the reflection of the lighting
> direction about the normal. And furthermore, we'll raise the cosine to
> some power, so you can control how shiny the surface is, how white the
> highlight is. There is an alternative form which just says, takes the
> half angle between the light source and the viewer, and take the dot
> product of that with the normal. So, then it's much closer to standard
> diffuse illumination, which is the dot product of light and normal,
> this is dot product of the half angle and normal, and again you can
> raise it to some power. That's something which is known as the
> Blinn-Phong model and actually for physical surfaces, the half-angle
> form is more accurate. It's the form in standard OpenGL and largely,
> what I ask you to implement. Let first consider the standard Phong
> formula, not the Blinn-Phong form, where you're considering the
> reflection of the light direction about the normal, that is the angles
> are the same and it's in a plane. That's why I can draw this diagram
> on a plane. And now I am looking at really, the angle between the
> reflected direction and the eye. This is between the reflected
> direction and the eye. And that angle, that cosine I am going to now
> raise to some power. Okay. So the question is, I just need to find the
> mathematical formula for the reflected direction. And it's relatively
> easy to do it, although the formula is somewhat complex. So we first
> look at the lighting direction. And I'm going to break this into the
> horizontal and the vertical components, so the vertical component is
> along the direction of the normal, the horizontal component is going
> along the surface. Now the horizontal component doesn't actually
> change for the reflection, but the vertical component, the direction,
> is changed and that's essentially what a reflection is. So you can
> take the original lighting which includes the parallel and the
> perpendicular component and what we want to do is flip this component
> along the normal. So you consider the component along the normal and
> you take twice that in order to flip it and you subtract. So
> essentially what we have is we have the lighting, then what you want
> to do is subtract out this component, so that will be the dot product
> of the lighting and the normal along the direction of the normal
> assuming all of these things are unit vectors. And you want to have a
> factor of 2 in there. So, I've just inverted the signs in order to
> make this work out and get the correct sign. But essentially that's
> what you have. You have 2 of L dot N times N, because that corresponds
> to the reflection, and then you subtract out the lighting. An
> alternative form is the half-angle form, which is the Blinn-Phong
> formula. And that's after Jim Blinn, who was one of the pioneers in
> computer graphics. Just tweak this formula a little bit, and there you
> just take the lighting and the reflected direction. You take
> half-angle between them, so you can look at H. If these were scalars
> would just be L plus R divided by 2. In our case, we can write it as L
> plus R, and you can normalize by the norm of L plus R. So what is the
> final specular reflection formula? You have some intensity for the
> light i, times the specular coefficient of the material, times the
> attenuation, times again max of N dot H, 0. Just as you had max of N
> dot L, 0, but there is this additional shininess term which controls
> how sharp the lobe is. So if shininess is very large, it's
> concentrated about the half angle direction and the mirror direction.
> If shininess is 0, then it essentially is very similar to the
> Lambertian case, except using the half angle instead of the lighting
> direction for the cosine. Okay. So let's do one example of this. Let's
> go through the mytest3 example. And here is my program. Okay. Now,
> what I want to do is change the intensity. So, let's look at this, and
> let me bring in my, editor. So, first of all I am going to make the
> teapot move a little bit faster, so I'll change this to .005. And then
> I want to change the intensity in the highlight, so right now the
> exponent is 100. Let's make the exponent equal to 10. Okay? So
> remember how the highlight looked like earlier. I'm going to show you
> writing actual code. So I come here and I say make mytest3. And it
> goes through the compilation and eventually it will make the program.
> So now all I need to do is run it. And you notice that the highlights
> are much larger. So let me make it the same size as the earlier, this
> one. And you notice that if you compare the highlights on this teapot
> here, which was my original program, to the highlights here, you'll
> see that the highlights have now become much larger. And of course, my
> teapot is moving somewhat more quickly because I made it move. I
> changed the increment. And so if I made the highlight back to 100 then
> I would get this. So this is with 10, this is with 100. And in this
> way you can shape the way in which the highlights look. In the next
> segment, we'll be talking about the fragment shaders, and ways in
> which you will actually implement this in OpenGL.