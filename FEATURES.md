# CPU Scheduling Simulator - Features

## ✅ Implemented Features

### 1. **Modern Dark-Themed UI**
- Glassmorphism design with backdrop blur effects
- Purple and pink gradient scheme
- Fully responsive layout (desktop, tablet, mobile)
- Smooth animations and transitions

### 2. **Process Management**
- **Quick Add Form**: Compact process input with Process ID, Arrival Time, and Burst Time
- **Tag-Style Process Display**: Processes shown as interactive badges
  - Visual pill-shaped tags with gradient backgrounds
  - Hover effects with elevation and shadow
  - Quick removal with × button
  - Detailed tooltip on hover (Arrival, Burst, Priority)
  - Animated entry transitions

### 3. **Scheduling Algorithms** (5 Different)
- **FCFS** (First Come First Served) - Non-preemptive
- **SJF** (Shortest Job First) - Non-preemptive
- **SRTF** (Shortest Remaining Time First) - Preemptive
- **Round Robin** - With configurable time quantum
- **Priority Scheduling** - Based on process priority

### 4. **Data Validation & Error Handling**
- Comprehensive validation before adding processes:
  - Non-empty field checks
  - Type validation (must be numbers)
  - Range validation (Arrival ≥ 0, Burst > 0, Priority ≥ 1)
- User-friendly toast notifications for errors
- Real-time validation during form submission

### 5. **Gantt Chart Visualization**
- **Flexbox-based layout** with proportional block widths
- **Color-coded processes**: Each process ID gets a unique, consistent color
- **Start/End time display**: Clear time labels on each execution block
- **Idle time handling**: Gray dashed blocks showing CPU idle periods
- **Time axis markers**: Numbered timeline below the chart
- **Hover effects**: Blocks highlight and expand on hover
- **Legend**: Visual indicators for process vs. idle blocks
- **Box shadows**: Subtle depth effect for better visual hierarchy

### 6. **Summary Statistics**
- **Average Waiting Time** (with total)
- **Average Turnaround Time** (with total)
- **CPU Utilization %** - Calculated as (Total Burst Time / Total Execution Time) × 100
- **Total Execution Time**
- All displayed in beautiful card-based layout with gradients

### 7. **Detailed Results Table**
- Process-by-process breakdown showing:
  - Arrival Time
  - Burst Time
  - Completion Time
  - Turnaround Time (in green)
  - Waiting Time (in pink)
- Color-coded rows for better readability
- Alternating row backgrounds
- Process names colored to match Gantt chart blocks

### 8. **Dynamic UI**
- **Conditional field display**:
  - Priority field shows only when "Priority" scheduling is selected
  - Time Quantum field shows only for "Round Robin" algorithm
  - Smooth expand/collapse animations
- **Algorithm information panel**: Contextual descriptions for each algorithm
- **Form state management**: Automatic reset after process addition

### 9. **Calculation Engine**
- **Completion Time (CT)** calculation
- **Turnaround Time (TAT)** = CT - Arrival Time
- **Waiting Time (WT)** = TAT - Burst Time
- **CPU Utilization** = (Total Burst / Total Time) × 100
- **Proper idle time detection** and visualization

### 10. **Code Quality**
- Well-documented functions with JSDoc comments
- Separation of concerns (validation, calculation, display)
- Responsive event handling
- Efficient color management system
- Helper functions for common operations (hexToRgb, getProcessColor)

## 📊 Metrics Calculated

For each process:
- **Arrival Time**: When process becomes ready
- **Burst Time**: CPU execution time needed
- **Completion Time**: When process finishes
- **Turnaround Time**: How long from arrival to completion
- **Waiting Time**: Time spent waiting in queue

System-wide:
- **Average Waiting Time**: Sum of all waiting times / number of processes
- **Average Turnaround Time**: Sum of all turnaround times / number of processes
- **CPU Utilization**: Percentage of time CPU is actively executing (not idle)
- **Total Execution Time**: Time from first arrival to last completion

## 🎨 Design Features

- **Dark theme** with vibrant accent colors
- **Gradient overlays** for depth
- **Smooth transitions** (0.3s ease)
- **Responsive grid layouts** with auto-fit columns
- **Color-coded data visualization**:
  - Purple/blue for primary elements
  - Green for positive metrics (turnaround)
  - Pink for additional metrics (waiting)
  - Gray for idle time
- **Card-based design** for information grouping
- **Interactive elements** with hover states
- **Accessibility-friendly** with good contrast ratios

## 🔧 Algorithm Details

### FCFS
- Simplest algorithm
- Processes execute in arrival order
- Can cause "convoy effect" with long processes blocking short ones

### SJF
- Minimizes average waiting time
- Selects shortest job among ready processes
- Starts next job only when current completes

### SRTF
- Preemptive version of SJF
- Checks on each time unit if shorter job arrived
- More complex scheduling overhead

### Round Robin
- Fair scheduling with time quantum
- Each process gets equal CPU time slice
- Remaining processes rejoin queue if not complete

### Priority
- Executes based on priority value (lower = higher priority)
- Good for giving importance to critical tasks
- Can suffer from starvation of low-priority processes

## 💾 File Structure

```
/home/tharnis/Documents/OS project/
├── cpu_scheduling_simulator.html (Single-file application)
└── FEATURES.md (This file)
```

## 🚀 How to Use

1. **Open the HTML file** in any modern web browser
2. **Add processes** using the Quick Add form:
   - Enter Process ID (e.g., P1, P2)
   - Set Arrival Time (when process arrives)
   - Set Burst Time (how long it needs to run)
   - Priority is auto-shown for priority scheduling
3. **Select a scheduling algorithm** from the dropdown
4. **Adjust time quantum** if using Round Robin
5. **Click "Run Simulation"** to see results
6. **View the Gantt Chart** showing execution timeline
7. **Review metrics table** with detailed per-process statistics
8. **Compare algorithms** by running multiple simulations
9. **Reset** to clear and start over

## 🎯 Learning Outcomes

This simulator helps understand:
- How different scheduling algorithms work
- Impact on waiting time and turnaround time
- CPU utilization improvements
- Context switching (especially in preemptive algorithms)
- Real-world scheduling challenges

---

**Created**: February 21, 2026
**Version**: 1.0
**Status**: ✅ Production Ready
