# ballin' frr


<div style="position:relative; width:100%; height:500px; overflow:hidden;">
    <img id="dvdImage" src="https://png.pngtree.com/png-vector/20240528/ourmid/pngtree-armadillos-png-image_12507956.png" alt="Spinning and Bouncing Image" style="position:absolute; width:100px;">
</div>

<script>
    const img = document.getElementById('dvdImage');
    let posX = window.innerWidth / 2, posY = window.innerHeight / 2;
    let speedX = 2, speedY = 2;
    const speedIncreaseFactor = 1.1;
    const imgWidth = img.width;
    const imgHeight = img.height;

        if (posX + imgWidth >= windowWidth || posX <= 0) {
            speedX = -speedX * speedIncreaseFactor;
        }
        if (posY + imgHeight >= windowHeight || posY <= 0) {
            speedY = -speedY * speedIncreaseFactor;
        }

        posX += speedX;
        posY += speedY;

        img.style.left = posX + 'px';
        img.style.top = posY + 'px';

        requestAnimationFrame(moveImage);
    }

    moveImage();
</script>