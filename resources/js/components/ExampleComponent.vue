<template>
 <h2 class="border">wavy</h2>
<h2 class="wave">wavy</h2>

<h2 class="border two">wavy</h2>
<h2 class="wave two">wavy</h2>

<h2 class="border three">wavy</h2>
<h2 class="wave three">wavy</h2>
</template>

<script>
    export default {
        mounted() {
            console.log('Component mounted.')
        }
    }
</script>
<style lang=scss>
@import url('https://fonts.googleapis.com/css2?family=Work+Sans:wght@400;500;600;700&display=swap');

/* * {
	margin: 0;
	padding: 0;
}

body {
	font-family: "Work Sans", sans-serif;
	letter-spacing: 2vmin;
	background: black;
	display: flex;	
	height: 100vh;
	width: 100vw;
	align-items: center;
	justify-content: center;
}

h2 {
	font-size: 15vmin;
	position: absolute;
} */

.border {
	color: rgb(68, 16, 119);  
  text-shadow:
    -1px -1px 0 white, 
    1px -1px 0 white,
    -1px 1px 0 white,
    1px 1px 0 white;  
}

.wave {
	color: white;
	animation: wave 3s ease-in-out infinite;
}

.two {
	transform: translateY(0.8em);
}

.three {
	transform: translateY(-0.8em);
}

@keyframes wave {
	0%, 100% {
		clip-path: polygon(0% 47%, 10% 48%, 33% 54%, 54% 60%, 70% 61%, 84% 59%, 100% 52%, 100% 100%, 0% 100%);
	}

	50% {
		clip-path: polygon(0% 60%, 15% 65%, 34% 66%, 51% 62%, 67% 50%, 84% 45%, 100% 46%, 100% 100%, 0% 100%);
	}
}

</style>

