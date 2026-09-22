<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AR Profile - Klao paksekune</title>
    <!-- A-Frame และ AR.js -->
    <script src="https://aframe.io/releases/1.4.0/aframe.min.js"></script>
    <script src="https://raw.githack.com/AR-js-org/AR.js/master/aframe/build/aframe-ar.js"></script>
    <style>
        body { margin: 0; overflow: hidden; font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; }
        
        /* สไตล์กล่อง About me (กรอบใส ขอบสีขาวเทา) */
        #about-box {
            position: absolute;
            bottom: 30px;
            left: 50%;
            transform: translateX(-50%);
            z-index: 10;
            background: rgba(255, 255, 255, 0.15);
            backdrop-filter: blur(8px);
            -webkit-backdrop-filter: blur(8px);
            border: 2px solid rgba(220, 220, 220, 0.6);
            border-radius: 12px;
            padding: 15px 25px;
            color: #ffffff;
            text-align: center;
            box-shadow: 0 8px 32px 0 rgba(0, 0, 0, 0.37);
            max-width: 90%;
            width: 350px;
        }
        #about-box h2 {
            margin: 0 0 8px 0;
            font-size: 1.2rem;
            letter-spacing: 1px;
            color: #f0f0f0;
            text-transform: uppercase;
        }
        #about-box p {
            margin: 0;
            font-size: 0.95rem;
            line-height: 1.4;
            color: #e0e0e0;
        }
    </style>
</head>
<body>

    <!-- กล่องข้อความ About me -->
    <div id="about-box">
        <h2>About Me</h2>
        <p><strong>Klao paksekune</strong><br>3D Modeling & Character Design (2D/3D)</p>
    </div>

    <!-- ฉาก AR และ 3D Scene -->
    <a-scene embedded arjs>
        
        <!-- แสงสว่างในฉาก -->
        <a-light type="ambient" color="#b0e0e6" intensity="0.8"></a-light>
        <a-light type="directional" color="#fffaed" position="-1 2 1" intensity="1.2"></a-light>

        <!-- ท้องฟ้าสีฟ้าออกเขียว ปลอดโปร่ง ไม่มีเมฆ -->
        <a-sky color="#66a3a3"></a-sky>

        <!-- AR Marker (ใช้ Hiro เป็นค่าเริ่มต้น สามารถเปลี่ยนเป็นรูปแบบอื่นได้ตามต้องการ) -->
        <a-marker preset="hiro">
            
            <!-- พื้นทะเลทราย -->
            <a-plane position="0 0 0" rotation="-90 0 0" width="12" height="12" color="#d4b278" roughness="0.9"></a-plane>

            <!-- ซากปรักหักพังกระจายตัว (ขนาดเล็กและใหญ่) -->
            <a-box position="-1.5 0.1 -1" width="0.8" height="0.4" depth="0.6" color="#8c7853" rotation="0 25 10"></a-box>
            <a-box position="1.2 0.2 -1.5" width="1.2" height="0.6" depth="1.0" color="#736142" rotation="0 -15 -5"></a-box>
            <a-box position="0.5 0.05 1.0" width="0.4" height="0.2" depth="0.5" color="#8c7853" rotation="10 40 0"></a-box>
            <a-cylinder position="-1.0 0.3 0.8" radius="0.2" height="0.6" color="#615238" rotation="15 0 25"></a-cylinder>
            <a-box position="-0.8 0.08 -1.8" width="0.5" height="0.15" depth="0.5" color="#736142" rotation="5 10 -8"></a-box>

            <!-- สิ่งมีชีวิตคล้ายควายขายาวทรงหลอมเหลว (ตรงกลาง) ตามเรฟเฟอเรนซ์ภาพ[cite: 2] -->
            <a-entity id="creature-container" position="0 0 0">
                
                <!-- ลำตัวโครงกระดูก (สีแดงสดเงางามแบบของเหลว) -->
                <a-box position="0 1.2 -0.2" width="0.3" height="0.3" depth="1.2" color="#ff0022" roughness="0.2" metalness="0.8">
                    <a-animation attribute="rotation" dur="3000" direction="alternate" repeat="indefinite" to="0 5 0"></a-animation>
                </a-box>

                <!-- ขายาวเรียวและเหลว -->
                <a-cylinder position="-0.3 0.6 -0.6" radius="0.03" height="1.2" color="#e60019" roughness="0.3"></a-cylinder>
                <a-cylinder position="0.3 0.6 -0.6" radius="0.03" height="1.2" color="#e60019" roughness="0.3"></a-cylinder>
                <a-cylinder position="-0.25 0.6 0.4" radius="0.03" height="1.2" color="#e60019" roughness="0.3"></a-cylinder>
                <a-cylinder position="0.25 0.6 0.4" radius="0.03" height="1.2" color="#e60019" roughness="0.3"></a-cylinder>

                <!-- เขาโค้งยาวอันเป็นเอกลักษณ์ -->
                <a-torus position="0 1.5 -0.8" radius="0.4" radius-tubular="0.02" arc="270" color="#ff1a3c" rotation="0 90 45"></a-torus>

            </a-entity>

        </a-marker>

        <!-- กล้องสำหรับ AR -->
        <a-entity camera></a-entity>
    </a-scene>

    <!-- Script ควบคุมให้สิ่งมีชีวิตหันจ้องมองตามเคอร์เซอร์เมาส์ -->
    <script>
        const creature = document.querySelector('#creature-container');
        
        window.addEventListener('mousemove', (event) => {
            // คำนวณพิกัดตำแหน่งเมาส์บนหน้าจอ
            const mouseX = (event.clientX / window.innerWidth) * 2 - 1;
            const mouseY = -(event.clientY / window.innerHeight) * 2 + 1;

            // สั่งให้โมเดลขยับหมุนตามทิศทางเมาส์ที่ผู้ใช้เลื่อน
            creature.setAttribute('rotation', `${mouseY * 15} ${mouseX * 30} 0`);
        });
    </script>
</body>
</html>
