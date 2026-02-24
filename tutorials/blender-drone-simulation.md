# Step-by-Step: Setting Up a Basic Drone Simulation in Blender

**Create a realistic drone swarm in Blender using only built-in tools — no coding required.**

This tutorial shows you how to simulate hundreds of drones flocking together like birds. It is ideal for visual explanations, presentations, or understanding swarm behavior.

### Prerequisites
- Blender 4.2 or later (free at blender.org)
- 15–20 minutes

### Step 1: Prepare the Scene
1. Open Blender and delete the default cube (select it → X → Delete).
2. Add a large ground plane: Shift + A → Mesh → Plane.
3. Scale it up: S → 50 → Enter (creates a 100 m × 100 m flight area).

![Step 1: Ground plane setup](assets/blender-step1.jpg)

### Step 2: Create a Simple Drone Model
1. Add a Cube for the body: Shift + A → Mesh → Cube.
2. Scale it flat: S → Z → 0.2, S → X → 0.5, S → Y → 0.5.
3. Add 4 thin cylinders for arms (Shift + A → Mesh → Cylinder, scale and position at corners).
4. Select all parts → Ctrl + J to join.
5. Set origin: Right-click → Set Origin → Origin to Geometry.

![Step 2: Low-poly drone model](assets/blender-step2.jpg)

### Step 3: Set Up the Particle System
1. Select the ground plane.
2. Go to the Particle Properties tab (right panel) → New.
3. Set Number: 300 (or more for a bigger swarm).
4. Set Lifetime: 500 (long animation).
5. Under Render → Render As: Object.
6. Instance Object: select your drone model.

![Step 3: Particle system](assets/blender-step3.jpg)

### Step 4: Enable Boids Physics for Flocking
1. Change Physics type to **Boids**.
2. In Boids Brain, add these rules (in order):
   - Separate (strength 1.0) — keeps drones apart.
   - Align (strength 1.0) — makes them fly the same direction.
   - Cohesion (strength 1.0) — keeps the group together.
3. Set Max Velocity to 5.0 for realistic drone speed.



### Step 5: Add Movement (Optional Goal)
1. Add an Empty (Shift + A → Empty → Plain Axes).
2. Keyframe its movement across the scene (frame 1 and frame 300).
3. In Boids Brain, add a Goal rule and target the Empty.

### Step 6: Bake and Play
1. In Particle Cache → Bake.
2. Play the timeline (Spacebar) to watch the swarm flock.

### Step 7: Polish with Lights and Camera
- Add emission materials to propellers for glowing lights.
- Position a camera for a dynamic fly-through shot.
- Add a Sun light or HDRi for realistic lighting.

### Step 8: Render
Set output to FFmpeg Video and render (Ctrl + F12).

### Why this matters
This simple setup demonstrates the same three boids rules (separation, alignment, cohesion) we covered in the drone swarm explainer. You can now create compelling visuals that help non-technical audiences understand swarm technology.

<image-card alt="Step 1" src="../assets/blender-step1.jpg" ></image-card>
<image-card alt="Step 2" src="../assets/blender-step2.jpg" ></image-card>
<image-card alt="Step 3" src="../assets/blender-step3.jpg" ></image-card>
<image-card alt="Step 4: Boids rules" src="../assets/blender-step4.jpg" ></image-card>

