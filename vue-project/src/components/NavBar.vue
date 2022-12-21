<template>
    <div class="header">
        <img src="./icons/Netflix_logo.svg.png" width="130" alt="imagen del nav bar">
        <div class="navBar">
            <nav>
                 <ul>
                   <li>Inicio</li>
                   <li>Estrenos</li>
                    <li>Tendencias</li>
                    <li>Series</li>
                    <li>Películas</li>
                </ul>
             </nav>
         </div>
        </div>

</template>

<script>

</script>

<style>

.header{
    background-color:rgb(79, 147, 167);
    color: white;
    display: flex;
    justify-content: space-between;
    margin-right: 0px;
    margin-left: 0px;
    font-weight: 900;
}

.navBar{
    margin-left: 50px;
}

nav ul li {
    list-style: none;
    margin-left: 75px;
    padding: 25px 0;
    padding-right: 30px;
    float: left;
}

</style>