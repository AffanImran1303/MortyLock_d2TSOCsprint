<!-- component -->
<link href="https://unpkg.com/tailwindcss@^2/dist/tailwind.min.css" rel="stylesheet">
<script>
let email = '';                                                                                                                                                    let username ='';
  let password = '';

  async function register() {
    const response = await fetch('https://morty-lock-d2-tso-csprint.vercel.app/api/auth/register', {
      method: 'POST',
      headers: { 'Content-Type': 'application/json' },
      body: JSON.stringify({ email, username, password })
    });

    const data = await response.json();
    if (response.ok) {
      // Handle success (e.g., redirect to login page)
    } else {
      // Handle error
      console.error(data.message);
    }
  }
</script>


<div class="relative min-h-screen flex items-center justify-center bg-transparent py-12 px-4 sm:px-6 lg:px-8 bg-transparent bg-no-repeat bg-cover relative items-center">
	<div class="absolute opacity-100 inset-0 z-0"></div>
	<div class="max-w-md w-full space-y-8 p-10 bg-white rounded-xl border-2 border-[#3d76d9] z-10">
		<div class="text-center">
			<h2 class="mt-6 text-3xl font-bold">
				New User?
			</h2>
			<p class="mt-2 text-sm">Get your account registered!</p>
		</div>
        
		<form class="mt-8 space-y-6" action="#" method="POST" on:submit|preventDefault={register}>
			<input type="hidden" name="remember" value="true">
			<div class="relative">

				<label class="text-sm font-bold tracking-wide">Username
				<input class=" w-full text-base py-2 border-b border-gray-300 focus:outline-none focus:border-blue-600" type="" placeholder="Enter username" value="">
            </label>    
            </div>
            <div class="mt-8 content-center">
				<label class="text-sm font-bold tracking-wide">
					Email
				
				<input class="w-full content-center text-base py-2 border-b border-gray-300 focus:outline-none focus:border-blue-600" type="email" placeholder="Enter your Email" bind:value={email} required>
            </label>
            </div>
			<div class="mt-8 content-center">
				<label class="text-sm font-bold tracking-wide">
					Password
				
				<input class="w-full content-center text-base py-2 border-b border-gray-300 focus:outline-none focus:border-blue-600" type="password" placeholder="Enter your password" bind:value={password} required>
            </label>
            </div>
            <div class="mt-8 content-center">
				<label class="text-sm font-bold tracking-wide">
					Confirm Password
				
				<input class="w-full content-center text-base py-2 border-b border-gray-300 focus:outline-none focus:border-blue-600" type="" placeholder="Re-enter your password" value="">
            </label>
            </div>
			<div>
				<button type="submit" class="primary-button w-full flex justify-center p-4  rounded-lg tracking-wide
                                font-semibold  focus:outline-none focus:shadow-outline hover:bg-[#29478a] shadow-lg cursor-pointer transition ease-in duration-300">
                    Register
                </button>
			</div>
			<p class="flex flex-col items-center justify-center mt-10 text-center text-md text-gray-500">
				<span>Already have an account?</span>
				<a href="login" class="text-[#29478a] hover:text-blue-500no-underline hover:underline cursor-pointer transition ease-in duration-300">Login</a>
			</p>
		</form>
	</div>
</div>