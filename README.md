# Tutorial Overview
In this tutorial, students will program two Lite 6 robot arms to pass marbles to each other using a dual spiral marble slide. Each robot will wait for a bumper switch signal, retrieve its marble from the bottom of the slide, place it at the top of the partner's slide, trigger the partner's bumper switch, and return to a waiting position.

# Learning Objectives
- Use manual mode to map robot arm positions
- Understand sequence programming with block code
- Implement wait/trigger logic with sensors
- Practice precision positioning with robotic manipulators

# Equipment Needed (per pair of arms)
- 2x Lite 6 robot arms (facing each other)
- 1x dual spiral marble slide
- 2x bumper switches
- 2x marbles
- Computer with robot control software

# Procedure

## Part 1: Setup and Manual Positioning (15-20 min)
Students will use manual mode to find and record key positions:

**Required positions for EACH arm:**
1. **Home/Waiting position** - Safe position away from workspace
2. **Marble pickup position** - Gripper at bottom of OWN slide chute
3. **Marble dropoff position** - Gripper at top of PARTNER's slide chute
4. **Bumper switch press position** - Extended to press partner's switch

**Task:** Move the arm manually to each position and record the coordinates/joint angles.

## Part 2: Program Logic (20-25 min)

**Program structure (same for both arms):**
```
FOREVER
├─ Move to Home position
├─ WAIT for bumper switch press
├─ Wait 2 seconds (adjust as needed)
├─ Move to Marble pickup position
├─ Close gripper (grab marble)
├─ Move to Marble dropoff position  
├─ Open gripper (release marble)
├─ Move to Bumper switch press position
└─ (loop repeats automatically)
```

**Key programming concepts:**
- **Forever block** - Contains the entire sequence, runs continuously
- **Wait blocks** - Robot pauses until bumper switch is triggered
- **Movement blocks** - Use saved positions from Part 1
- **Gripper blocks** - Open/close to grab and release
- **Timing** - Add delays so marble has time to roll down

## Part 3: Testing and Refinement (10-15 min)
- Test each arm individually first
- Adjust positions if marble is dropped or missed
- Test with human pressing bumper switches
- If time allows: test both arms in sequence

# Safety Reminders
- Keep hands clear when arms are moving
- Use emergency stop if needed
- One person operates controls, one person observes
- Start with slow speed settings

# Troubleshooting
| Problem | Solution |
|---------|----------|
| Arm drops marble | Adjust gripper close strength or position |
| Arm misses marble | Re-record pickup position in manual mode |
| Marble doesn't trigger switch | Check switch placement and arm reach |
| Button not responsive | Check program is using correct configurable input (e.g. CI 4) |

# Extensions (if students finish early)
- Run both arms simultaneously with two marbles
- Have the arm do a wave motion after delivering the marble
- Count successful passes
- Time how long full cycle takes
