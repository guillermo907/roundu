<template>
    <div class="home">
        <div class="custom-shape-divider-top-1617511854">
            <svg data-name="Layer 1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 120" preserveAspectRatio="none">
                <path d="M1200 0L0 0 892.25 114.72 1200 0z" class="shape-fill"></path>
            </svg>
        </div>
        <div class="content">
            <h1>Round U</h1>
            <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Obcaecati, nisi porro. Ducimus, reiciendis blanditiis 
                cumque, laborum, consectetur eius sit ipsum quo minus explicabo quisquam. Necessitatibus accusantium obcaecati atque, 
                illum modi explicabo debitis amet, 
                sed doloremque voluptas neque magnam vitae nam numquam. Fugiat, sunt at architecto iste quae dolor hic sed?</p>
        </div>
        <div class="custom-shape-divider-bottom-1617512758">
            <svg data-name="Layer 1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 120" preserveAspectRatio="none">
                <path d="M1200 0L0 0 892.25 114.72 1200 0z" class="shape-fill"></path>
            </svg>
        </div> 
    </div>
</template>

<script>
export default {
    name: "Home"
}
</script>

<style scoped>
.home{
    --div-color: #2c3e50;

    position: relative;
    display: flex;
    align-items: center;
    justify-content: center;
    background-color:rgb(243, 243, 243);
    background-image: url('https://images.unsplash.com/photo-1617375112754-3b599e496376?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1050&q=80');
    background-size: 100%;
    background-blend-mode: overlay;
    min-height: 90vh;
}
.content{
    
    max-width: 55%;
}
p{
    font-family: 'Nothing You Could Do', cursive;
}
.custom-shape-divider-top-1617511854 {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    overflow: hidden;
    line-height: 0;
}

.custom-shape-divider-top-1617511854 .shape-fill {
    fill: var(--div-color);
}
.custom-shape-divider-bottom-1617512758 {
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
    overflow: hidden;
    line-height: 0;
    transform: rotate(180deg);
}

.custom-shape-divider-bottom-1617512758 svg {
    position: relative;
    display: block;
    width: calc(128% + 1.3px);
    height: 154px;
}

.custom-shape-divider-bottom-1617512758 .shape-fill {
    fill: var(--div-color);
}
</style>