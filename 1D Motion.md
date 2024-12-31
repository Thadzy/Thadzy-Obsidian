#Physics 
[[2D, 3D Motion]]
## How to solve the problem in Physics
1. What the problem given?
2. Visualization
3. What does the amount means?
## Define Calculus
![[Pasted image 20241022110240.png | 600]]
>**Is it necessary to select a contact point to calculate the slope?**
>>*Ans* No, it is not necessary to select a specific contact point to calculate the slope of a graph. The slope can be determined by choosing any two points on the graph, calculating the differences and using them to find the slope (mm) of the tangent line. $m = \frac{\Delta y}{\Delta x}$

>**How to select that 2 points?**
>>*Ans* To find the slope of a tangent to a curve, need to approximate the tangent line. Choose two points that are very close to the point of interest (the contact point) to estimate the slope of the tangent line.
## Visualization the movement of the particle
![[Pasted image 20241022112218.png]]
>**At t = 20 Does the particle return and Why it return?**
>>*Ans* Yes, because of at t= 20 the displacement is going back the graph is decreasing 
>>*Key point*
>>- When the graph is increasing (slope > 0), the particle is moving away from its initial position.
>>- When the graph is decreasing (slope < 0), the particle is returning or moving back toward its starting point.
## Main
### Wording
- **Speed** -> is defined as the distance traveled per unit of time. It is a scalar quantity
$$\frac{Distance}{Time}$$
- **Velocity** -> on the other hand, refers to the rate of change of displacement, which includes both magnitude and direction. It is a vector quantity,
$$\frac{Displacement}{Time}$$
- **Distance** -> is the total length of the path traveled by an object, regardless of direction. It is a scalar quantity
- **Displacement** -> is the shortest straight-line distance from the initial position to the final position of an object.

>**What does at any given moment mean? For example t = 15**
>>*Ans* Just like the $\Delta$ But $\lim_{x \to 0}$ in small time --> Calculus 

>**Average speed = instantaneous speed or not?**
>>*Ans* No because Average speed is all the speed has one value but the instantaneous speed also the 1 value at the specific moment in time.
### How to find instantaneous speed
1. Close 2 points $\Delta t \to 0$
2. Find $\Delta X, \Delta T$
3. V = $\frac{\Delta X}{\Delta T}$ but $\Delta T \to 0$
4. V = $\lim_{\Delta t \to 0} \frac{\Delta X}{\Delta T}$ = $\frac{dx}{dt}$
## Acceleration
Tell how fast the speed is changing
$$ a = \frac{\Delta v}{\Delta t} = \frac{dv}{dt}$$ 
### Acceleration direction
V -> A -> Accerate
V <- A -> Delay
## Turning point
Turning point is the $\frac{dx}{dt} = 0$ (v = 0) is the particle still have the speed it's can't return
>**What if particle have speed can it return?**
>>*Ans* If a particle has speed (i.e., $\frac{dz}{dt} \neq 0$), it means that the particle is still in motion. The ability of a particle to return to a previous position depends on several factors:
1. **Direction of Motion**:
    - If the particle is moving in the opposite direction towards a previous position, it can return without any issue.
    - If it is moving away from that position, it cannot return until its direction changes.
2. **Forces Acting on the Particle**:
    - If external forces (like gravity, friction, or applied forces) act on the particle, they can influence its motion. For instance:
        - A particle thrown upwards will eventually slow down due to gravity, stop at its peak (a turning point), and then return to its original position.
        - A particle moving in a frictionless environment may continue indefinitely unless acted upon by another force.
3. **Energy Considerations**:
    - In conservative systems (like a pendulum), energy conservation allows the particle to return to its original position after reaching maximum height.
    - In non-conservative systems (like one with significant friction), energy loss can prevent the particle from returning.

![[Pasted image 20241022120930.png | 600]]
![[Pasted image 20241022121025.png]]
The relationship of the graph is when v = 0, x change direction
## Motion Graph
![[Pasted image 20241231171609.png | 600]]
### Position-Time Graph
- **Slope**: Represents velocity (V).
- **Area**: Not directly applicable or meaningful.
- **Formula**: $V=\frac{ΔX}{Δt}$​ (change in position over time).
### Velocity-Time Graph
- **Slope**: Represents acceleration (a).
- **Area**: Represents change in position $\Delta X$.
- **Formula**: $s=v⋅t$ (displacement as velocity times time).
### Acceleration-Time Graph
- **Slope**: Not provided (typically jerk in physics).
- **Area**: Represents change in velocity $\Delta V$.
- **Formula**: $\Delta V = at$ (change in velocity as acceleration times time).