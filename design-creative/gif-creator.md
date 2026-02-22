---
name: gif-creator
description: "Create animated GIFs optimized for Slack and web. Provides constraints, validation, and animation concepts. Use when users request animated GIFs."
source: https://github.com/anthropics/skills
---

# GIF Creator

Create animated GIFs optimized for Slack and web.

## Requirements

**Slack Emoji GIFs:**
- Dimensions: 128x128
- FPS: 10-30 (lower = smaller file)
- Colors: 48-128
- Duration: Under 3 seconds

**Message/Web GIFs:**
- Dimensions: 480x480
- More flexibility on duration

## Core Workflow

```python
from PIL import Image, ImageDraw

# 1. Create frames
frames = []
for i in range(12):
    frame = Image.new('RGB', (128, 128), (240, 248, 255))
    draw = ImageDraw.Draw(frame)

    # Draw animation frame
    # Use PIL primitives: ellipse, polygon, line, rectangle

    frames.append(frame)

# 2. Save GIF
frames[0].save(
    'output.gif',
    save_all=True,
    append_images=frames[1:],
    duration=100,  # ms per frame
    loop=0
)
```

## Drawing Graphics

### PIL Primitives

```python
draw = ImageDraw.Draw(frame)

# Circles/ovals
draw.ellipse([x1, y1, x2, y2], fill=(r, g, b), outline=(r, g, b), width=3)

# Stars, triangles, polygons
points = [(x1, y1), (x2, y2), (x3, y3)]
draw.polygon(points, fill=(r, g, b), outline=(r, g, b))

# Lines
draw.line([(x1, y1), (x2, y2)], fill=(r, g, b), width=5)

# Rectangles
draw.rectangle([x1, y1, x2, y2], fill=(r, g, b))
```

### Making Graphics Look Good

- **Use thick lines** - Always `width=2` or higher
- **Add visual depth** - Gradients, layers, highlights
- **Make shapes interesting** - Add rings, patterns, glows
- **Use vibrant colors** - Complementary, with contrast

## Animation Concepts

### Shake/Vibrate
```python
offset_x = math.sin(i * 0.5) * 5
offset_y = math.cos(i * 0.7) * 3
```

### Pulse/Heartbeat
```python
scale = 1.0 + 0.2 * math.sin(i * 0.5)
```

### Bounce
```python
# Easing function
t = i / num_frames
y = start_y + (end_y - start_y) * ease_bounce(t)
```

### Spin/Rotate
```python
angle = i * (360 / num_frames)
rotated = image.rotate(angle, resample=Image.BICUBIC)
```

### Fade In/Out
```python
alpha = int(255 * (i / num_frames))  # fade in
alpha = int(255 * (1 - i / num_frames))  # fade out
```

### Slide
```python
x = start_x + (end_x - start_x) * ease_out(t)
```

### Explode/Particle Burst
```python
for particle in particles:
    particle.x += particle.vx
    particle.y += particle.vy
    particle.vy += gravity
    particle.alpha -= fade_rate
```

## Easing Functions

```python
def ease_out(t):
    return 1 - (1 - t) ** 3

def ease_in_out(t):
    if t < 0.5:
        return 4 * t ** 3
    return 1 - (-2 * t + 2) ** 3 / 2

def bounce_out(t):
    if t < 1/2.75:
        return 7.5625 * t * t
    elif t < 2/2.75:
        t -= 1.5/2.75
        return 7.5625 * t * t + 0.75
    elif t < 2.5/2.75:
        t -= 2.25/2.75
        return 7.5625 * t * t + 0.9375
    else:
        t -= 2.625/2.75
        return 7.5625 * t * t + 0.984375
```

## Optimization

When file size matters:

1. **Fewer frames** - 10 FPS instead of 20
2. **Fewer colors** - 48 instead of 128
3. **Smaller dimensions** - 128x128 instead of 480x480
4. **Remove duplicate frames**

```python
# Optimized save
frames[0].save(
    'output.gif',
    save_all=True,
    append_images=frames[1:],
    duration=100,
    loop=0,
    optimize=True
)
```

## Dependencies

```bash
pip install pillow imageio numpy
```
