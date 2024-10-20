<!-- <div class="navbar bg-[#29478a] text-[#fefdfd]">
    <div class="navbar-start">
      <div class="dropdown">
        <div tabindex="0" role="button" class="btn btn-ghost lg:hidden">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            class="h-5 w-5"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor">
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M4 6h16M4 12h8m-8 6h16" />
          </svg>
        </div>
        <ul
          class="menu menu-sm dropdown-content bg-base-100 rounded-box z-[1] mt-3 w-52 p-2 shadow">
          <li><a href="/">Home</a></li>
          <li><a href="login">Login</a></li>
          <li><a href="registration">Register</a></li>
        </ul>
      </div>
      <div>
      <a href="/">
      <span class="text-xl font-bold">MortyLock</span></a>
      </div>
    </div>
    <div class="navbar-end">
        <div class="navbar-center hidden lg:flex">
            <ul class="menu menu-horizontal font-semibold">
              <li><a href="/" class="mx-2">Home</a></li>  
              <li><a href="login" class="mx-2">Login</a></li>
              <li><a href="registration" class="bg-emerald-600 text-white mx-2">Register</a></li>
            </ul>
          </div>
    </div>
  </div> -->
<div class="flex justify-center">
  <div class="navbar bg-[#29478a] text-[#fefdfd] w-96% rounded-lg m-5">
    <div class="navbar-start">
      <div class="dropdown">
        <div tabIndex={0} role="button" class="btn btn-ghost lg:hidden">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            class="h-5 w-5"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor">
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M4 6h16M4 12h8m-8 6h16" />
          </svg>
        </div>
        <ul
          tabIndex={0}
          class="menu menu-sm dropdown-content bg-[#3d76d9] text-white rounded-box z-[1] mt-3 w-52 p-2 shadow">
          <li><a href="/">Home</a></li>
        </ul>
      </div>
      <a class="btn btn-ghost text-xl font-semibold" href="/">MortyLock</a>
    </div>
    <div class="navbar-center hidden lg:flex">
      <ul class="menu menu-horizontal px-1">
        <li><a href="/">Home</a></li>
      </ul>
    </div>
    <div class="navbar-end">
      <a class="btn secondary-button" href="login">Login</a>
      <a class="btn m-2 primary-button" href="registration">Get Register</a>

    </div>
    
  </div>
</div>