document.addEventListener('DOMContentLoaded', () => {
    const slides = document.querySelectorAll('.slide');
    const prevButton = document.getElementById('prev-slide');
    const nextButton = document.getElementById('next-slide');
    let currentSlideIndex = 0;

    function updateSlideCount() {
        slides.forEach((slide, index) => {
            const footer = slide.querySelector('footer');
            if (footer) {
                footer.textContent = `슬라이드 ${index + 1} / ${slides.length}`;
            }
        });
    }

    function showSlide(index) {
        slides.forEach((slide, i) => {
            slide.classList.remove('active');
            if (i === index) {
                slide.classList.add('active');
            }
        });
        // Disable/enable buttons
        prevButton.disabled = index === 0;
        nextButton.disabled = index === slides.length - 1;
    }

    prevButton.addEventListener('click', () => {
        if (currentSlideIndex > 0) {
            currentSlideIndex--;
            showSlide(currentSlideIndex);
        }
    });

    nextButton.addEventListener('click', () => {
        if (currentSlideIndex < slides.length - 1) {
            currentSlideIndex++;
            showSlide(currentSlideIndex);
        }
    });
    
    updateSlideCount();
    showSlide(currentSlideIndex);

    // D3.js Visualization Stubs
    // Slide 4: Basic Spacetime Fabric
    const spacetimeViz = d3.select("#spacetime-fabric-viz");
    if (!spacetimeViz.empty()) {
        const svgWidth = spacetimeViz.node().clientWidth;
        const svgHeight = spacetimeViz.node().clientHeight;
        const svg = spacetimeViz.append("svg")
            .attr("width", svgWidth)
            .attr("height", svgHeight);

        const gridSize = 20;
        for (let i = 0; i <= svgWidth; i += gridSize) {
            svg.append("line")
               .attr("x1", i).attr("y1", 0)
               .attr("x2", i).attr("y2", svgHeight)
               .attr("stroke", "#4a4a68").attr("stroke-width", 0.5);
        }
        for (let i = 0; i <= svgHeight; i += gridSize) {
            svg.append("line")
               .attr("x1", 0).attr("y1", i)
               .attr("x2", svgWidth).attr("y2", i)
               .attr("stroke", "#4a4a68").attr("stroke-width", 0.5);
        }
    }

    // Slide 5: Mattress and Bowling Ball
    const mattressViz = d3.select("#mattress-bowlingball-viz");
    let fabricSVG, fabricLines, massCircle;
    if (!mattressViz.empty()) {
        const svgWidth = mattressViz.node().clientWidth;
        const svgHeight = mattressViz.node().clientHeight;
        fabricSVG = mattressViz.append("svg")
            .attr("width", svgWidth)
            .attr("height", svgHeight);
        
        const gridSize = 20;
        const numX = Math.floor(svgWidth / gridSize);
        const numY = Math.floor(svgHeight / gridSize);
        let points = [];

        for (let y = 0; y <= numY; y++) {
            for (let x = 0; x <= numX; x++) {
                points.push({ x: x * gridSize, y: y * gridSize, ox: x * gridSize, oy: y * gridSize });
            }
        }

        fabricLines = fabricSVG.append("g");

        function drawFabric(currentPoints) {
            fabricLines.selectAll("*").remove(); // Clear previous lines
            // Horizontal lines
            for (let y = 0; y <= numY; y++) {
                for (let x = 0; x < numX; x++) {
                    fabricLines.append("line")
                        .attr("x1", currentPoints[y * (numX + 1) + x].x)
                        .attr("y1", currentPoints[y * (numX + 1) + x].y)
                        .attr("x2", currentPoints[y * (numX + 1) + (x + 1)].x)
                        .attr("y2", currentPoints[y * (numX + 1) + (x + 1)].y)
                        .attr("stroke", "#4a4a68").attr("stroke-width", 1);
                }
            }
            // Vertical lines
            for (let x = 0; x <= numX; x++) {
                for (let y = 0; y < numY; y++) {
                     fabricLines.append("line")
                        .attr("x1", currentPoints[y * (numX + 1) + x].x)
                        .attr("y1", currentPoints[y * (numX + 1) + x].y)
                        .attr("x2", currentPoints[(y + 1) * (numX + 1) + x].x)
                        .attr("y2", currentPoints[(y + 1) * (numX + 1) + x].y)
                        .attr("stroke", "#4a4a68").attr("stroke-width", 1);
                }
            }
        }
        drawFabric(points); // Initial draw

        window.addMassToFabric = function() {
            if (massCircle) massCircle.remove(); // Remove old one
            
            const massX = svgWidth / 2;
            const massY = svgHeight / 2;
            const massStrength = 80; // How much it pulls
            const massRadius = 15;

            massCircle = fabricSVG.append("circle")
                .attr("cx", massX)
                .attr("cy", massY)
                .attr("r", massRadius)
                .attr("fill", "#9fa8da");

            let newPoints = points.map(p => {
                const dx = p.ox - massX;
                const dy = p.oy - massY;
                const distance = Math.sqrt(dx * dx + dy * dy);
                if (distance === 0) return { ...p, x: p.ox, y: p.oy }; // Avoid division by zero
                
                // Pull points towards the mass, effect diminishes with distance
                const pullFactor = Math.max(0, massStrength / (distance * 0.5 + massStrength * 0.1));
                // Don't let points go inside the mass visually
                const maxPull = Math.max(0, distance - massRadius * 0.8); 

                return {
                    ...p,
                    x: p.ox - (dx / distance) * Math.min(maxPull, pullFactor),
                    y: p.oy - (dy / distance) * Math.min(maxPull, pullFactor)
                };
            });
            drawFabric(newPoints);
        };

        window.resetFabric = function() {
            if (massCircle) massCircle.remove();
            massCircle = null;
            drawFabric(points.map(p => ({...p, x:p.ox, y:p.oy})));
        };
    }

    // Slide 6: Gravity and Marbles (Conceptual - using existing fabric)
    const gravityMarblesViz = d3.select("#gravity-marbles-viz");
    if(!gravityMarblesViz.empty()){
        // This would build on the previous visualization.
        // For simplicity, we'll just add a text placeholder for now.
        gravityMarblesViz.html("<p style='color:#ccc; padding:10px;'>Imagine marbles rolling on the deformed fabric above. They would follow the curves!</p>");
        // To actually animate marbles:
        // 1. Calculate gradient of the deformed surface.
        // 2. Simulate marble movement based on this gradient.
    }
    window.addMarbles = function() {
        if (!massCircle || !fabricSVG) {
            alert("먼저 볼링공을 놓아 시공간을 왜곡시켜주세요.");
            return;
        }
        // Add a few small "marble" circles
        const marbleRadius = 5;
        const massX = parseFloat(massCircle.attr("cx"));
        const massY = parseFloat(massCircle.attr("cy"));

        for (let i=0; i<3; i++) {
            const startX = Math.random() * fabricSVG.attr("width") * 0.2 + fabricSVG.attr("width")*0.1; // Start near an edge
            const startY = Math.random() * fabricSVG.attr("height");
            
            fabricSVG.append("circle")
                .attr("class", "marble")
                .attr("cx", startX)
                .attr("cy", startY)
                .attr("r", marbleRadius)
                .attr("fill", "orange")
                .transition()
                .duration(2000 + Math.random()*1000)
                .ease(d3.easeQuadIn) // Accelerate towards
                .attr("cx", massX + (Math.random()-0.5)*30) // End up near the mass
                .attr("cy", massY + (Math.random()-0.5)*30)
                .remove(); // Remove after animation
        }
    }


    // Slide 7: Time Dilation Clocks
    let clockIntervalWeak, clockIntervalStrong;
    let timeWeak = 0, timeStrong = 0;
    const clockWeakEl = document.getElementById('clock-weak');
    const clockStrongEl = document.getElementById('clock-strong');

    function formatTime(totalSeconds) {
        const hours = Math.floor(totalSeconds / 3600);
        const minutes = Math.floor((totalSeconds % 3600) / 60);
        const seconds = totalSeconds % 60;
        return `${String(hours).padStart(2, '0')}:${String(minutes).padStart(2, '0')}:${String(seconds).padStart(2, '0')}`;
    }

    window.startTimeDilationDemo = function() {
        clearInterval(clockIntervalWeak);
        clearInterval(clockIntervalStrong);
        timeWeak = 0; timeStrong = 0;
        clockWeakEl.textContent = formatTime(0);
        clockStrongEl.textContent = formatTime(0);

        // Weak gravity clock ticks "normally" (e.g., every 100ms in demo time)
        clockIntervalWeak = setInterval(() => {
            timeWeak++;
            clockWeakEl.textContent = formatTime(timeWeak);
        }, 100); // 1 "second" per 100ms

        // Strong gravity clock ticks slower (e.g., every 200ms in demo time)
        clockIntervalStrong = setInterval(() => {
            timeStrong++;
            clockStrongEl.textContent = formatTime(timeStrong);
        }, 200); // 1 "second" per 200ms (half the speed)
    };


});
