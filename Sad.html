<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>3D Portfolio - Klao paksekune</title>
    <style>
        body {
            margin: 0;
            overflow: hidden;
            background-color: #66a3a3;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        /* สไตล์กล่อง About me (มุมซ้ายบน กรอบใส ขอบสีขาวเทา) */
        #about-box {
            position: absolute;
            top: 25px;
            left: 25px;
            z-index: 10;
            background: rgba(255, 255, 255, 0.12);
            backdrop-filter: blur(10px);
            -webkit-backdrop-filter: blur(10px);
            border: 2px solid rgba(220, 220, 220, 0.5);
            border-radius: 12px;
            padding: 20px;
            color: #ffffff;
            box-shadow: 0 8px 32px 0 rgba(0, 0, 0, 0.3);
            max-width: 320px;
            pointer-events: none; /* ให้เมาส์ทะลุผ่านไปควบคุม 3D ด้านหลังได้ */
        }
        #about-box h1 {
            margin: 0 0 6px 0;
            font-size: 1.25rem;
            letter-spacing: 0.5px;
            color: #ffffff;
            text-transform: uppercase;
        }
        #about-box h2 {
            margin: 0 0 10px 0;
            font-size: 1rem;
            color: #ffcccc;
            font-weight: 500;
        }
        #about-box p {
            margin: 0;
            font-size: 0.9rem;
            line-height: 1.4;
            color: #e0e0e0;
        }
    </style>
</head>
<body>

    <!-- กล่องข้อความ About me บริเวณซ้ายบน -->
    <div id="about-box">
        <h1>About Me</h1>
        <h2>Klao paksekune</h2>
        <p>3D Modeling & Character Design (2D/3D)</p>
    </div>

    <!-- โหลด Three.js จาก CDN -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>

    <script>
        // --- 1. SETUP SCENE, CAMERA, RENDERER ---
        const scene = new THREE.Scene();
        // ท้องฟ้าสีฟ้าออกเขียว ปลอดโปร่ง ไม่มีเมฆ
        scene.background = new THREE.Color(0x66a3a3);
        scene.fog = new THREE.FogExp2(0x66a3a3, 0.035);

        const camera = new THREE.PerspectiveCamera(60, window.innerWidth / window.innerHeight, 0.1, 1000);
        camera.position.set(0, 3, 7);
        camera.lookAt(0, 1, 0);

        const renderer = new THREE.WebGLRenderer({ antialias: true });
        renderer.setSize(window.innerWidth, window.innerHeight);
        renderer.setPixelRatio(window.devicePixelRatio);
        document.body.appendChild(renderer.domElement);

        // --- 2. LIGHTING ---
        const ambientLight = new THREE.AmbientLight(0xd1f0f0, 0.7);
        scene.add(ambientLight);

        const dirLight = new THREE.DirectionalLight(0xfffaed, 1.2);
        dirLight.position.set(5, 10, 7);
        scene.add(dirLight);

        // --- 3. ENVIRONMENT (DESERT & RUINS) ---
        // พื้นทะเลทราย
        const floorGeo = new THREE.PlaneGeometry(100, 100);
        const floorMat = new THREE.MeshStandardMaterial({ color: 0xd4b278, roughness: 0.9 });
        const floor = new THREE.Mesh(floorGeo, floorMat);
        floor.rotation.x = -Math.PI / 2;
        scene.add(floor);

        // ซากปรักหักพังกระจายตัว (เศษเล็กและขนาดใหญ่รอบฉาก)
        const ruinMat = new THREE.MeshStandardMaterial({ color: 0x826d4e, roughness: 0.8 });
        const ruinGeos = [
            new THREE.BoxGeometry(1.2, 0.6, 0.8),
            new THREE.BoxGeometry(0.5, 1.5, 0.5),
            new THREE.BoxGeometry(0.8, 0.3, 1.2),
            new THREE.CylinderGeometry(0.3, 0.4, 1.0, 6),
            new THREE.BoxGeometry(0.4, 0.4, 0.4)
        ];

        for (let i = 0; i < 25; i++) {
            const geo = ruinGeos[Math.floor(Math.random() * ruinGeos.length)];
            const ruin = new THREE.Mesh(geo, ruinMat);
            
            // สุ่มตำแหน่งรอบๆ โดยเว้นตรงกลางไว้ให้สิ่งมีชีวิต
            const angle = Math.random() * Math.PI * 2;
            const radius = 2.5 + Math.random() * 8;
            ruin.position.set(Math.cos(angle) * radius, 0.2, Math.sin(angle) * radius);
            
            ruin.rotation.set(Math.random() * Math.PI, Math.random() * Math.PI, Math.random() * Math.PI);
            scene.add(ruin);
        }

        // --- 4. CREATURE (สิ่งมีชีวิตคล้ายควายขายาวหลอมเหลวสีแดง) ---
        const creatureGroup = new THREE.Group();
        scene.add(creatureGroup);
        creatureGroup.position.set(0, 0, 0);

        // วัสดุของเหลวสีแดงเงางาม (ตามภาพเรฟเฟอเรนซ์)[cite: 2]
        const fluidRedMat = new THREE.MeshStandardMaterial({ 
            color: 0xff0022, 
            roughness: 0.15, 
            metalness: 0.85 
        });

        // ลำตัวและโครงกระดูก (ตรงกลาง)
        const bodyGeo = new THREE.CylinderGeometry(0.12, 0.15, 1.8, 8);
        bodyGeo.rotateZ(Math.PI / 2);
        const body = new THREE.Mesh(bodyGeo, fluidRedMat);
        body.position.set(0, 1.6, 0);
        creatureGroup.add(body);

        // หัวสิ่งมีชีวิต
        const headGeo = new THREE.ConeGeometry(0.2, 0.7, 7);
        headGeo.rotateX(Math.PI / 2);
        const head = new THREE.Mesh(headGeo, fluidRedMat);
        head.position.set(0, 1.7, -1.0);
        creatureGroup.add(head);

        // เขายาวโค้งอันเป็นเอกลักษณ์
        const hornGeo = new THREE.TorusGeometry(0.4, 0.03, 8, 30, Math.PI * 1.3);
        const leftHorn = new THREE.Mesh(hornGeo, fluidRedMat);
        leftHorn.position.set(-0.15, 1.9, -1.0);
        leftHorn.rotation.z = Math.PI / 4;
        creatureGroup.add(leftHorn);

        const rightHorn = new THREE.Mesh(hornGeo, fluidRedMat);
        rightHorn.position.set(0.15, 1.9, -1.0);
        rightHorn.rotation.z = -Math.PI / 4;
        creatureGroup.add(rightHorn);

        // ขายาวเรียวและเหลว (4 ขา)
        const legGeo = new THREE.CylinderGeometry(0.04, 0.02, 1.7, 6);
        const legPositions = [
            [-0.4, 0.85, -0.7], // หน้าซ้าย
            [ 0.4, 0.85, -0.7], // หน้าขวา
            [-0.35, 0.85,  0.6], // หลังซ้าย
            [ 0.35, 0.85,  0.6]  // หลังขวา
        ];

        const legs = [];
        legPositions.forEach(pos => {
            const leg = new THREE.Mesh(legGeo, fluidRedMat);
            leg.position.set(...pos);
            creatureGroup.add(leg);
            legs.push(leg);
        });

        // --- 5. MOUSE INTERACTION & ANIMATION ---
        let mouseX = 0;
        let mouseY = 0;
        let targetRotationX = 0;
        let targetRotationY = 0;

        window.addEventListener('mousemove', (event) => {
            // แปลงพิกัดเมาส์เป็นค่า -1 ถึง 1
            mouseX = (event.clientX / window.innerWidth) * 2 - 1;
            mouseY = -(event.clientY / window.innerHeight) * 2 + 1;
        });

        const clock = new THREE.Clock();

        function animate() {
            requestAnimationFrame(animate);

            const elapsedTime = clock.getElapsedTime();

            // อนิเมชันการหายใจ/บิดตัวเบาๆ ของสิ่งมีชีวิต
            creatureGroup.position.y = Math.sin(elapsedTime * 2) * 0.05;
            body.rotation.y = Math.sin(elapsedTime * 1.5) * 0.05;

            // คำนวณการหันตามเคอร์เซอร์เมาส์อย่างนุ่มนวล (Smooth damping)
            targetRotationY = mouseX * 0.6;
            targetRotationX = -mouseY * 0.3;

            creatureGroup.rotation.y += (targetRotationY - creatureGroup.rotation.y) * 0.08;
            creatureGroup.rotation.x += (targetRotationX - creatureGroup.rotation.x) * 0.08;

            renderer.render(scene, camera);
        }

        animate();

        // --- 6. RESIZE WINDOW HANDLING ---
        window.addEventListener('resize', () => {
            camera.aspect = window.innerWidth / window.innerHeight;
            camera.updateProjectionMatrix();
            renderer.setSize(window.innerWidth, window.innerHeight);
        });
    </script>
</body>
</html>
