# READ.ME
import math
import random
import cairo
import imageio
import numpy as np

WIDTH, HEIGHT = 512, 512
NUM_FRAMES = 1000
SPARKLE_FACTOR = 1  # Increase this value for more sparkly effect

def draw_frame(surface, frame_num):
    ctx = cairo.Context(surface)
    ctx.scale(WIDTH, HEIGHT)

    # Background
    ctx.rectangle(0, 0, 1, 1)
    ctx.set_source_rgb(0, 0, 0)
    ctx.fill()

    # Stars
    for _ in range(3 * SPARKLE_FACTOR):  # More stars for a sparkly effect
        x = random.random()
        y = random.random()
        size = (random.random() + 1) / 2 * 0.01
        ctx.arc(x, y, size, 0, 2 * math.pi)
        ctx.set_source_rgb(1, 1, 1)
        ctx.fill()

    # Glitter
    for _ in range(5 * SPARKLE_FACTOR):  # More glitter for a sparkly effect
        x = random.random()
        y = random.random()
        size = (random.random() + 1) / 2 * 0.02
        ctx.arc(x, y, size, 0, 2 * math.pi)
        ctx.set_source_rgb(1, 1, 0)
        ctx.fill()

images = []
for frame_num in range(NUM_FRAMES + 1):  # Add one extra frame for the loop
    surface = cairo.ImageSurface(cairo.FORMAT_ARGB32, WIDTH, HEIGHT)
    draw_frame(surface, frame_num)

    # Convert the cairo surface to a numpy array
    buf = surface.get_data()
    arr = np.ndarray(shape=(HEIGHT, WIDTH, 4), buffer=buf, dtype=np.uint8)

    images.append(arr)

# Create loopable gif by appending the first frame to the end
images.append(images[0])

# Create gif
imageio.mimsave('glittery_star_loop.gif', images, duration=0.2)

$\text{\color{#B22222} Moe/vessel/rochas/user or nosoi}$\
$\text{\color{#FFFAA0} idk how to program ts hep}$\
$\text{\color{#6FC276} transmasc pls use my pronouns!! He/they}$\
$\text{\color{#000080} i love my children broooo i love them smm }$
$\text{\color{#553311} c+h LOVER}$\
$\text{\color{#aa7733} moztly watching yt or zitting with oomffzz}$\
$\text{\color{#dd9955} don't be mean to me or my friendz brah!!😡}$

$\text{\color{#FFAA00} wip ok? ok.. huge moe fiction kin doubles intt<3}$

$\text{\color{#b41314} iwc if your rude or hateful}$ 

$\text{\color{#555555} i've been getting really irritated easily lately zo iwec if my name says "upset" :D}$
