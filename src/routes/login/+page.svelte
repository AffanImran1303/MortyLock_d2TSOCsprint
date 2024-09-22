<!-- component -->
<link href="https://unpkg.com/tailwindcss@^2/dist/tailwind.min.css" rel="stylesheet">
<div class="relative min-h-screen flex items-center justify-center bg-transparent py-12 px-4 sm:px-6 lg:px-8 bg-transparent bg-no-repeat bg-cover relative items-center">
	<div class="absolute opacity-100 inset-0 z-0"></div>
	<div class="max-w-md w-full space-y-8 p-10 bg-white rounded-xl z-10">
		<div class="text-center">
			<h2 class="mt-6 text-3xl font-bold text-gray-900">
				Welcome Back!
			</h2>
			<p class="mt-2 text-sm text-gray-600">Please sign in to your account</p>
		</div>
        
		<form class="mt-8 space-y-6" action="#" method="POST">
			<input type="hidden" name="remember" value="true">
			<div class="relative">

				<label class="text-sm font-bold text-gray-700 tracking-wide">Email
				<input class=" w-full text-base py-2 border-b border-gray-300 focus:outline-none focus:border-emerald-600" type="" placeholder="Enter your email" value="">
            </label>    
            </div>
			<div class="mt-8 content-center">
				<label class="text-sm font-bold text-gray-700 tracking-wide">
					Password
				
				<input class="w-full content-center text-base py-2 border-b border-gray-300 focus:outline-none focus:border-emerald-600" type="" placeholder="Enter your password" value="">
            </label>
            </div>
			<div class="flex items-center justify-between">
					<div class="flex items-center">
						<input id="remember_me" name="remember_me" type="checkbox" class="h-4 w-4 bg-indigo-500 focus:ring-indigo-400 border-gray-300 rounded">
						<label for="remember_me" class="ml-2 block text-sm text-gray-900">
                            Remember me
                        </label>
					</div>
				<div class="text-sm">
					<a href="." class="font-medium text-emerald-600 hover:text-indigo-500">
								Forgot your password?
					</a>
				</div>
			</div>
			<div>
				<button type="submit" class="w-full flex justify-center bg-emerald-600 text-gray-100 p-4  rounded-lg tracking-wide
                                font-semibold  focus:outline-none focus:shadow-outline hover:bg-emerald-400 shadow-lg cursor-pointer transition ease-in duration-300">
                    Login
                </button>
			</div>
			<p class="flex flex-col items-center justify-center mt-10 text-center text-md text-gray-500">
				<span>Don't have an account?</span>
				<a href="registration" class="text-emerald-600 hover:text-indigo-500no-underline hover:underline cursor-pointer transition ease-in duration-300">Get registered</a>
			</p>
		</form>
	</div>
</div>