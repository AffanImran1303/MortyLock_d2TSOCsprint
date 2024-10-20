<!-- component -->
<link href="https://unpkg.com/tailwindcss@^2/dist/tailwind.min.css" rel="stylesheet">

<script>
let email = '';
let password = '';
let token = '';

async function login() {
  const response = await fetch('https://morty-lock-d2-tso-csprint.vercel.app/api/auth/login', {
	method: 'POST',
	headers: { 'Content-Type': 'application/json' },
	body: JSON.stringify({ email, password })
  });

  const data = await response.json();
  if (response.ok) {
	token = data.access_token;  // Store the JWT token
	// Store token in local storage or session storage
	localStorage.setItem('authToken', token);
  } else {
	// Handle login failure
	console.error(data.message);
  }
}
</script>

<div class="relative min-h-screen flex items-center justify-center py-12 px-4 sm:px-6 lg:px-8 bg-transparent bg-no-repeat bg-cover relative items-center">
	<div class="absolute opacity-100 inset-0 z-0"></div>
	<div class="max-w-md w-full space-y-8 p-10 bg-white rounded-xl border-2 border-[#3d76d9] z-10">
		<div class="text-center">
			<h2 class="mt-6 text-3xl font-bold">
				Welcome Back!
			</h2>
			<p class="mt-2 text-sm">Please sign in to your account</p>
		</div>
        
		<form class="mt-8 space-y-6" action="#" method="POST" on:submit|preventDefault={login}>
			<input type="hidden" name="remember" value="true">
			<div class="relative">

				<label class="text-sm font-bold tracking-wide">Email
				<input class=" w-full py-2 border-b border-gray-300 focus:outline-none focus:border-blue-600" type="email" placeholder="Enter your email" value={email} required>
            </label>    
            </div>
			<div class="mt-8 content-center">
				<label class="text-sm font-bold tracking-wide">
					Password
				
				<input class="w-full content-center py-2 border-b border-gray-300 focus:outline-none focus:border-blue-600" type="password" placeholder="Enter your password" bind:value={password} required>
            </label>
            </div>
			<div class="flex items-center justify-between">
					<div class="flex items-center">
						<input id="remember_me" name="remember_me" type="checkbox" class="h-4 w-4 bg-indigo-500 focus:ring-blue-400 border-blue-500 rounded">
						<label for="remember_me" class="ml-2 block text-sm">
                            Remember me
                        </label>
					</div>
				<div class="text-sm">
					<a href="." class="font-medium hover:text-indigo-500">
								Forgot your password?
					</a>
				</div>
			</div>
			<div>
				<button type="submit" class="primary-button w-full flex justify-center text-gray-100 p-4  rounded-lg tracking-wide
                                font-semibold  focus:outline-none focus:shadow-outline hover:bg-blue-400 shadow-lg cursor-pointer transition ease-in duration-300">
                    Login
                </button>
			</div>
			<p class="flex flex-col items-center justify-center mt-10 text-center text-md text-gray-500">
				<span>Don't have an account?</span>
				<a href="registration" class="text-[#29478a] hover:text-blue-500 no-underline hover:underline cursor-pointer transition ease-in duration-300">Get registered</a>
			</p>
		</form>
	</div>
</div>