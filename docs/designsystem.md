<!-- Design System -->
<!DOCTYPE html>

<html class="light" lang="en"><head>
<meta charset="utf-8"/>
<meta content="width=device-width, initial-scale=1.0" name="viewport"/>
<title>DevCook - Login</title>
<script src="https://cdn.tailwindcss.com?plugins=forms,container-queries"></script>
<link href="https://fonts.googleapis.com/css2?family=Epilogue:wght@400;600;700&amp;family=Plus+Jakarta+Sans:wght@400;500;600&amp;display=swap" rel="stylesheet"/>
<link href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:wght,FILL@100..700,0..1&amp;display=swap" rel="stylesheet"/>
<link href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:wght,FILL@100..700,0..1&amp;display=swap" rel="stylesheet"/>
<script id="tailwind-config">
        tailwind.config = {
            darkMode: "class",
            theme: {
                extend: {
                    "colors": {
                        "secondary": "#006d37",
                        "on-error-container": "#93000a",
                        "on-primary-container": "#502600",
                        "on-surface-variant": "#564337",
                        "on-tertiary-fixed": "#2b1700",
                        "primary-container": "#e67e22",
                        "on-surface": "#091d2e",
                        "outline-variant": "#dcc1b1",
                        "surface-bright": "#f7f9ff",
                        "tertiary": "#865300",
                        "on-error": "#ffffff",
                        "on-secondary-fixed-variant": "#005228",
                        "primary-fixed-dim": "#ffb783",
                        "surface-container-high": "#d9eaff",
                        "on-secondary": "#ffffff",
                        "on-secondary-fixed": "#00210c",
                        "primary": "#944a00",
                        "on-secondary-container": "#007239",
                        "surface": "#f7f9ff",
                        "tertiary-fixed-dim": "#ffb961",
                        "secondary-container": "#7bf8a1",
                        "inverse-on-surface": "#e8f2ff",
                        "primary-fixed": "#ffdcc5",
                        "surface-container": "#e3efff",
                        "inverse-primary": "#ffb783",
                        "secondary-fixed": "#7efba4",
                        "error-container": "#ffdad6",
                        "on-tertiary-container": "#482b00",
                        "inverse-surface": "#203243",
                        "tertiary-fixed": "#ffddb9",
                        "on-tertiary": "#ffffff",
                        "surface-container-highest": "#d1e4fb",
                        "error": "#ba1a1a",
                        "surface-tint": "#944a00",
                        "on-primary-fixed": "#301400",
                        "secondary-fixed-dim": "#61de8a",
                        "surface-variant": "#d1e4fb",
                        "on-background": "#091d2e",
                        "tertiary-container": "#d78800",
                        "on-tertiary-fixed-variant": "#663e00",
                        "surface-container-low": "#edf4ff",
                        "background": "#f7f9ff",
                        "on-primary-fixed-variant": "#713700",
                        "surface-dim": "#c9dcf3",
                        "outline": "#897365",
                        "on-primary": "#ffffff",
                        "surface-container-lowest": "#ffffff"
                    },
                    "borderRadius": {
                        "DEFAULT": "1rem",
                        "lg": "2rem",
                        "xl": "3rem",
                        "full": "9999px"
                    },
                    "spacing": {
                        "sm": "12px",
                        "lg": "40px",
                        "margin-mobile": "16px",
                        "gutter": "24px",
                        "md": "24px",
                        "xs": "4px",
                        "xl": "64px",
                        "base": "8px",
                        "container-max": "1200px"
                    },
                    "fontFamily": {
                        "headline-lg-mobile": ["Epilogue"],
                        "display-lg": ["Epilogue"],
                        "label-md": ["Plus Jakarta Sans"],
                        "headline-md": ["Epilogue"],
                        "caption": ["Plus Jakarta Sans"],
                        "body-md": ["Plus Jakarta Sans"],
                        "body-lg": ["Plus Jakarta Sans"],
                        "headline-lg": ["Epilogue"]
                    },
                    "fontSize": {
                        "headline-lg-mobile": ["28px", { "lineHeight": "36px", "fontWeight": "600" }],
                        "display-lg": ["48px", { "lineHeight": "56px", "letterSpacing": "-0.02em", "fontWeight": "700" }],
                        "label-md": ["14px", { "lineHeight": "20px", "letterSpacing": "0.01em", "fontWeight": "600" }],
                        "headline-md": ["24px", { "lineHeight": "32px", "fontWeight": "600" }],
                        "caption": ["12px", { "lineHeight": "16px", "fontWeight": "500" }],
                        "body-md": ["16px", { "lineHeight": "24px", "fontWeight": "400" }],
                        "body-lg": ["18px", { "lineHeight": "28px", "fontWeight": "400" }],
                        "headline-lg": ["32px", { "lineHeight": "40px", "letterSpacing": "-0.01em", "fontWeight": "600" }]
                    }
                },
            },
        }
    </script>
<style>
        .squishy-btn {
            transition: transform 0.1s cubic-bezier(0.4, 0, 0.2, 1), box-shadow 0.1s cubic-bezier(0.4, 0, 0.2, 1);
        }
        .squishy-btn:active {
            transform: scale(0.96);
        }
        .glass-panel {
            background: rgba(247, 249, 255, 0.85);
            backdrop-filter: blur(16px);
            -webkit-backdrop-filter: blur(16px);
        }
    </style>
</head>
<body class="bg-background text-on-background min-h-screen flex items-center justify-center font-body-md relative overflow-hidden">
<!-- Background Image -->
<div class="absolute inset-0 z-0">
<div class="bg-cover bg-center w-full h-full opacity-60" data-alt="A modern, high-end lifestyle flatlay of a beautifully organized kitchen workspace viewed from above. The scene features a sleek wooden cutting board with fresh, vibrant vegetables like saffron threads, basil leaves, and bright orange carrots neatly arranged. Soft, natural sunlight streams in from the side, casting gentle shadows across a pristine white marble countertop. The overall aesthetic is clean, sophisticated, and warm, capturing the essence of culinary artistry and modern minimalism." style="background-image: url('https://lh3.googleusercontent.com/aida-public/AB6AXuBvki_JWnYM0edgc-IF0ptg4pWcRkp7LzWEoBuB5HANL60cpAlm5ugyey-T1E-7y-rm0Cv7y0GV-BVhqndSmaSW0aF9tva0WV87wy1EAdBX3iN_czolNMZzP9FbGLrT1lXuVXOdNX83pyHK41WUTjZ1pdnVJ8y0aBSlzHJFs69hgYQsqdcg1mLnWy9stoE3ipblEE-8ujfhu5d1MfrFvYhev6IGW880N7avxq6lwdgakhEyyxUqzjrUHw')"></div>
<div class="absolute inset-0 bg-gradient-to-br from-surface-bright/70 to-surface-variant/90 backdrop-blur-[2px]"></div>
</div>
<!-- Login Container -->
<main class="w-full max-w-md px-margin-mobile md:px-0 relative z-10">
<div class="glass-panel rounded-xl shadow-[0_8px_32px_rgba(148,74,0,0.08)] p-lg border border-outline-variant/30 flex flex-col gap-gutter">
<!-- Header -->
<div class="text-center mb-sm">
<h1 class="font-display-lg text-display-lg text-primary mb-2 tracking-tight">DevCook</h1>
<p class="font-body-lg text-body-lg text-on-surface-variant">Log in to your kitchen workspace.</p>
</div>
<!-- Error Message Placeholder (Hidden by default, shown for demonstration) -->
<div class="bg-error-container text-on-error-container p-sm rounded-lg flex items-center gap-sm border border-error/20" role="alert">
<span class="material-symbols-outlined" style="font-variation-settings: 'FILL' 1;">error</span>
<span class="font-caption text-caption">Invalid credentials. Please try again.</span>
</div>
<!-- Form -->
<form class="flex flex-col gap-md" onsubmit="event.preventDefault();">
<div class="flex flex-col gap-xs">
<label class="font-label-md text-label-md text-on-surface" for="email">Email Address</label>
<div class="relative">
<span class="material-symbols-outlined absolute left-sm top-1/2 -translate-y-1/2 text-on-surface-variant">mail</span>
<input class="w-full bg-surface-container-lowest border border-outline-variant rounded-full py-sm pl-xl pr-sm font-body-md text-body-md text-on-surface focus:outline-none focus:ring-2 focus:ring-primary focus:border-primary transition-shadow placeholder:text-on-surface-variant/50" id="email" name="email" placeholder="chef@devcook.io" required="" type="email"/>
</div>
</div>
<div class="flex flex-col gap-xs">
<div class="flex justify-between items-center">
<label class="font-label-md text-label-md text-on-surface" for="password">Password</label>
<a class="font-caption text-caption text-primary hover:text-primary-container transition-colors" href="#">Forgot password?</a>
</div>
<div class="relative">
<span class="material-symbols-outlined absolute left-sm top-1/2 -translate-y-1/2 text-on-surface-variant">lock</span>
<input class="w-full bg-surface-container-lowest border border-outline-variant rounded-full py-sm pl-xl pr-sm font-body-md text-body-md text-on-surface focus:outline-none focus:ring-2 focus:ring-primary focus:border-primary transition-shadow placeholder:text-on-surface-variant/50" id="password" name="password" placeholder="••••••••" required="" type="password"/>
</div>
</div>
<!-- Submit Button -->
<button class="squishy-btn w-full bg-primary text-on-primary font-label-md text-label-md py-md rounded-full shadow-[inset_0_2px_4px_rgba(255,255,255,0.2)] hover:bg-primary-container focus:outline-none focus:ring-4 focus:ring-primary-fixed/50 mt-sm flex justify-center items-center gap-xs" type="submit">
                    Enter Kitchen
                    <span class="material-symbols-outlined text-[18px]">arrow_forward</span>
</button>
</form>
<!-- Footer -->
<div class="text-center mt-sm">
<p class="font-body-md text-body-md text-on-surface-variant">
                    Don't have an account? 
                    <a class="font-label-md text-label-md text-primary hover:text-primary-container transition-colors" href="#">Sign up</a>
</p>
</div>
</div>
</main>
</body></html>

<!-- Login - DevCook -->
<!DOCTYPE html>

<html class="light" lang="en"><head>
<meta charset="utf-8"/>
<meta content="width=device-width, initial-scale=1.0" name="viewport"/>
<title>DevCook - Sign Up</title>
<script src="https://cdn.tailwindcss.com?plugins=forms,container-queries"></script>
<link href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:wght,FILL@100..700,0..1&amp;display=swap" rel="stylesheet"/>
<link href="https://fonts.googleapis.com/css2?family=Epilogue:wght@600;700&amp;family=Plus+Jakarta+Sans:wght@400;500;600&amp;display=swap" rel="stylesheet"/>
<link href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:wght,FILL@100..700,0..1&amp;display=swap" rel="stylesheet"/>
<script id="tailwind-config">
        tailwind.config = {
          darkMode: "class",
          theme: {
            extend: {
              "colors": {
                      "secondary": "#006d37",
                      "on-error-container": "#93000a",
                      "on-primary-container": "#502600",
                      "on-surface-variant": "#564337",
                      "on-tertiary-fixed": "#2b1700",
                      "primary-container": "#e67e22",
                      "on-surface": "#091d2e",
                      "outline-variant": "#dcc1b1",
                      "surface-bright": "#f7f9ff",
                      "tertiary": "#865300",
                      "on-error": "#ffffff",
                      "on-secondary-fixed-variant": "#005228",
                      "primary-fixed-dim": "#ffb783",
                      "surface-container-high": "#d9eaff",
                      "on-secondary": "#ffffff",
                      "on-secondary-fixed": "#00210c",
                      "primary": "#944a00",
                      "on-secondary-container": "#007239",
                      "surface": "#f7f9ff",
                      "tertiary-fixed-dim": "#ffb961",
                      "secondary-container": "#7bf8a1",
                      "inverse-on-surface": "#e8f2ff",
                      "primary-fixed": "#ffdcc5",
                      "surface-container": "#e3efff",
                      "inverse-primary": "#ffb783",
                      "secondary-fixed": "#7efba4",
                      "error-container": "#ffdad6",
                      "on-tertiary-container": "#482b00",
                      "inverse-surface": "#203243",
                      "tertiary-fixed": "#ffddb9",
                      "on-tertiary": "#ffffff",
                      "surface-container-highest": "#d1e4fb",
                      "error": "#ba1a1a",
                      "surface-tint": "#944a00",
                      "on-primary-fixed": "#301400",
                      "secondary-fixed-dim": "#61de8a",
                      "surface-variant": "#d1e4fb",
                      "on-background": "#091d2e",
                      "tertiary-container": "#d78800",
                      "on-tertiary-fixed-variant": "#663e00",
                      "surface-container-low": "#edf4ff",
                      "background": "#f7f9ff",
                      "on-primary-fixed-variant": "#713700",
                      "surface-dim": "#c9dcf3",
                      "outline": "#897365",
                      "on-primary": "#ffffff",
                      "surface-container-lowest": "#ffffff"
              },
              "borderRadius": {
                      "DEFAULT": "1rem",
                      "lg": "2rem",
                      "xl": "3rem",
                      "full": "9999px"
              },
              "spacing": {
                      "sm": "12px",
                      "lg": "40px",
                      "margin-mobile": "16px",
                      "gutter": "24px",
                      "md": "24px",
                      "xs": "4px",
                      "xl": "64px",
                      "base": "8px",
                      "container-max": "1200px"
              },
              "fontFamily": {
                      "headline-lg-mobile": ["Epilogue"],
                      "display-lg": ["Epilogue"],
                      "label-md": ["Plus Jakarta Sans"],
                      "headline-md": ["Epilogue"],
                      "caption": ["Plus Jakarta Sans"],
                      "body-md": ["Plus Jakarta Sans"],
                      "body-lg": ["Plus Jakarta Sans"],
                      "headline-lg": ["Epilogue"]
              },
              "fontSize": {
                      "headline-lg-mobile": ["28px", {"lineHeight": "36px", "fontWeight": "600"}],
                      "display-lg": ["48px", {"lineHeight": "56px", "letterSpacing": "-0.02em", "fontWeight": "700"}],
                      "label-md": ["14px", {"lineHeight": "20px", "letterSpacing": "0.01em", "fontWeight": "600"}],
                      "headline-md": ["24px", {"lineHeight": "32px", "fontWeight": "600"}],
                      "caption": ["12px", {"lineHeight": "16px", "fontWeight": "500"}],
                      "body-md": ["16px", {"lineHeight": "24px", "fontWeight": "400"}],
                      "body-lg": ["18px", {"lineHeight": "28px", "fontWeight": "400"}],
                      "headline-lg": ["32px", {"lineHeight": "40px", "letterSpacing": "-0.01em", "fontWeight": "600"}]
              }
            }
          }
        }
    </script>
<style>
        /* Smooth transitions for validation states */
        .validation-item { transition: color 0.3s ease; }
        .validation-item .material-symbols-outlined { transition: color 0.3s ease, transform 0.3s ease; }
        .valid { color: #007239; } /* on-secondary-container equivalent for visual feedback */
        .valid .material-symbols-outlined { color: #007239; transform: scale(1.1); }
        
        /* Custom input autofill override for modern look */
        input:-webkit-autofill,
        input:-webkit-autofill:hover, 
        input:-webkit-autofill:focus, 
        input:-webkit-autofill:active{
            -webkit-box-shadow: 0 0 0 30px #f7f9ff inset !important; /* surface-bright */
            -webkit-text-fill-color: #091d2e !important; /* on-surface */
            transition: background-color 5000s ease-in-out 0s;
        }
    </style>
</head>
<body class="bg-background text-on-background min-h-screen flex items-center justify-center p-margin-mobile md:p-lg antialiased">
<!-- Main Container: Fluid-Fixed Hybrid Split Layout -->
<main class="w-full max-w-container-max flex flex-col md:flex-row bg-surface rounded-lg shadow-[0_4px_40px_rgba(148,74,0,0.04)] overflow-hidden">
<!-- Left Side: Editorial Food Photography (Premium Aesthetic) -->
<div class="hidden md:block md:w-5/12 lg:w-1/2 relative bg-surface-container-high">
<div class="absolute inset-0 bg-cover bg-center" data-alt="A stunning, high-end editorial top-down photograph of premium culinary ingredients. A sleek white marble countertop is artfully arranged with vibrant saffron threads in a small ceramic bowl, fresh green basil leaves, whole peppercorns, and artisan pasta. Natural, bright, sun-drenched lighting casts soft, luxurious shadows, embodying a sophisticated modern cooking lifestyle." style="background-image: url('https://lh3.googleusercontent.com/aida-public/AB6AXuCd5Clh1hDDBIvAB1_6QVKAAuScMYo3zYdbzgj5GgynTTTOGn8YhTfebTOBVuR_WCJHenigo1f2xR_IE9p3gpJ6_9NaFlwbEU21xxhLNI6bbEwkbbR9J6haod8zV528YnDTfUmsuWF4yLT5IRXWn08sCDLeuZ7s64oOgBXX-0cnEh6ppnlKmCl1CRPRS7IJF6kD6jphFnpv13Ezhub8UKQJPVKc7NkZg5TTHu7K6o4lWCT152B6XEb2DA')"></div>
<!-- Gradient Overlay for subtle depth -->
<div class="absolute inset-0 bg-gradient-to-r from-transparent to-surface/90"></div>
<!-- Floating Brand Anchor -->
<div class="absolute top-lg left-lg">
<h1 class="font-headline-lg text-headline-lg text-on-surface flex items-center gap-xs">
<span class="material-symbols-outlined text-primary" style="font-variation-settings: 'FILL' 1;">restaurant_menu</span>
                    DevCook
                </h1>
</div>
</div>
<!-- Right Side: Sign Up Form -->
<div class="w-full md:w-7/12 lg:w-1/2 p-gutter md:p-lg lg:p-xl flex flex-col justify-center">
<div class="max-w-md mx-auto w-full">
<!-- Mobile Header Brand (Hidden on Desktop) -->
<h1 class="md:hidden font-headline-lg-mobile text-headline-lg-mobile text-on-surface flex items-center gap-xs mb-lg justify-center">
<span class="material-symbols-outlined text-primary" style="font-variation-settings: 'FILL' 1;">restaurant_menu</span>
                    DevCook
                </h1>
<div class="mb-lg text-center md:text-left">
<h2 class="font-headline-lg-mobile md:font-headline-lg text-headline-lg-mobile md:text-headline-lg text-on-surface mb-xs">Join the Kitchen</h2>
<p class="font-body-md text-body-md text-on-surface-variant">Start crafting your culinary masterpieces.</p>
</div>
<form class="flex flex-col gap-md" id="signup-form">
<!-- Name Field -->
<div class="flex flex-col gap-xs">
<label class="font-label-md text-label-md text-on-surface ml-sm" for="name">Full Name</label>
<div class="relative">
<span class="material-symbols-outlined absolute left-sm top-1/2 -translate-y-1/2 text-outline-variant">person</span>
<input class="w-full bg-surface-bright border-2 border-outline-variant/40 focus:border-primary rounded-full py-sm pl-[44px] pr-sm font-body-md text-body-md text-on-surface outline-none transition-all placeholder:text-outline shadow-sm focus:shadow-[0_0_15px_rgba(230,126,34,0.15)]" id="name" name="name" placeholder="Chef Developer" required="" type="text"/>
</div>
</div>
<!-- Email Field -->
<div class="flex flex-col gap-xs">
<label class="font-label-md text-label-md text-on-surface ml-sm" for="email">Email Address</label>
<div class="relative">
<span class="material-symbols-outlined absolute left-sm top-1/2 -translate-y-1/2 text-outline-variant">mail</span>
<input class="w-full bg-surface-bright border-2 border-outline-variant/40 focus:border-primary rounded-full py-sm pl-[44px] pr-sm font-body-md text-body-md text-on-surface outline-none transition-all placeholder:text-outline shadow-sm focus:shadow-[0_0_15px_rgba(230,126,34,0.15)]" id="email" name="email" placeholder="chef@devcook.com" required="" type="email"/>
</div>
</div>
<!-- Password Field & Hints -->
<div class="flex flex-col gap-xs">
<label class="font-label-md text-label-md text-on-surface ml-sm" for="password">Password</label>
<div class="relative">
<span class="material-symbols-outlined absolute left-sm top-1/2 -translate-y-1/2 text-outline-variant">lock</span>
<input class="w-full bg-surface-bright border-2 border-outline-variant/40 focus:border-primary rounded-full py-sm pl-[44px] pr-sm font-body-md text-body-md text-on-surface outline-none transition-all placeholder:text-outline shadow-sm focus:shadow-[0_0_15px_rgba(230,126,34,0.15)]" id="password" name="password" placeholder="••••••••" required="" type="password"/>
<button class="absolute right-sm top-1/2 -translate-y-1/2 text-outline hover:text-on-surface-variant transition-colors" id="toggle-password" type="button">
<span class="material-symbols-outlined text-[20px]">visibility</span>
</button>
</div>
<!-- Dev Console Style Validation Hints -->
<div class="bg-surface-container-lowest border border-outline-variant/30 rounded-[1rem] p-sm mt-xs grid grid-cols-2 gap-sm font-caption text-caption text-on-surface-variant shadow-sm">
<div class="validation-item flex items-center gap-xs" id="hint-length">
<span class="material-symbols-outlined text-[16px]">close</span>
<span>Min. 6 characters</span>
</div>
<div class="validation-item flex items-center gap-xs" id="hint-special">
<span class="material-symbols-outlined text-[16px]">close</span>
<span>1 Special character</span>
</div>
</div>
</div>
<!-- CEP / Address Field -->
<div class="flex flex-col gap-xs mt-sm">
<label class="font-label-md text-label-md text-on-surface ml-sm flex justify-between" for="cep">
                            Postal Code (CEP)
                            <span class="font-caption text-caption text-primary opacity-0 transition-opacity" id="cep-status">Fetching...</span>
</label>
<div class="relative">
<span class="material-symbols-outlined absolute left-sm top-1/2 -translate-y-1/2 text-outline-variant">location_on</span>
<input class="w-full bg-surface-bright border-2 border-outline-variant/40 focus:border-primary rounded-full py-sm pl-[44px] pr-sm font-body-md text-body-md text-on-surface outline-none transition-all placeholder:text-outline shadow-sm focus:shadow-[0_0_15px_rgba(230,126,34,0.15)] uppercase tracking-wider" id="cep" maxlength="9" name="cep" placeholder="00000-000" required="" type="text"/>
</div>
<!-- Automatic Address Display Area (Dev Console Style) -->
<div class="hidden flex-col gap-xs bg-surface-container border border-outline-variant/30 rounded-[1rem] p-sm mt-xs font-body-md text-body-md shadow-sm transition-all duration-300" id="address-display">
<div class="flex items-start gap-sm">
<span class="material-symbols-outlined text-primary mt-xs text-[20px]">home_pin</span>
<div class="flex flex-col">
<span class="text-on-surface font-medium" id="address-street">--</span>
<span class="text-on-surface-variant text-sm" id="address-neighborhood">--</span>
<span class="text-outline text-sm" id="address-city-state">--</span>
</div>
</div>
</div>
</div>
<!-- Submit Button -->
<button class="w-full bg-primary text-on-primary font-label-md text-label-md rounded-full py-4 mt-sm shadow-[inset_0_1px_1px_rgba(255,255,255,0.2),0_4px_10px_rgba(148,74,0,0.15)] hover:bg-surface-tint hover:shadow-[inset_0_1px_1px_rgba(255,255,255,0.2),0_6px_15px_rgba(148,74,0,0.25)] active:scale-[0.98] transition-all duration-200" type="submit">
                        Create Account
                    </button>
</form>
<!-- Footer Action -->
<div class="mt-lg text-center">
<a class="font-label-md text-label-md text-on-surface-variant hover:text-primary transition-colors flex items-center justify-center gap-xs" href="#">
<span class="material-symbols-outlined text-[18px]">arrow_back</span>
                        Back to login
                    </a>
</div>
</div>
</div>
</main>
<script>
        document.addEventListener('DOMContentLoaded', () => {
            // --- Password Validation Logic ---
            const passwordInput = document.getElementById('password');
            const togglePasswordBtn = document.getElementById('toggle-password');
            const toggleIcon = togglePasswordBtn.querySelector('.material-symbols-outlined');
            const hintLength = document.getElementById('hint-length');
            const hintSpecial = document.getElementById('hint-special');

            // Toggle visibility
            togglePasswordBtn.addEventListener('click', () => {
                const type = passwordInput.getAttribute('type') === 'password' ? 'text' : 'password';
                passwordInput.setAttribute('type', type);
                toggleIcon.textContent = type === 'password' ? 'visibility' : 'visibility_off';
            });

            // Validate on input
            passwordInput.addEventListener('input', (e) => {
                const val = e.target.value;
                
                // Length check (>= 6)
                if (val.length >= 6) {
                    hintLength.classList.add('valid');
                    hintLength.querySelector('.material-symbols-outlined').textContent = 'check';
                } else {
                    hintLength.classList.remove('valid');
                    hintLength.querySelector('.material-symbols-outlined').textContent = 'close';
                }

                // Special character check
                const specialCharRegex = /[!@#$%^&*(),.?":{}|<>]/;
                if (specialCharRegex.test(val)) {
                    hintSpecial.classList.add('valid');
                    hintSpecial.querySelector('.material-symbols-outlined').textContent = 'check';
                } else {
                    hintSpecial.classList.remove('valid');
                    hintSpecial.querySelector('.material-symbols-outlined').textContent = 'close';
                }
            });

            // --- CEP formatting & Mock Fetch Logic ---
            const cepInput = document.getElementById('cep');
            const cepStatus = document.getElementById('cep-status');
            const addressDisplay = document.getElementById('address-display');
            
            const addrStreet = document.getElementById('address-street');
            const addrNeighborhood = document.getElementById('address-neighborhood');
            const addrCityState = document.getElementById('address-city-state');

            // Format CEP as user types (00000-000)
            cepInput.addEventListener('input', (e) => {
                let value = e.target.value.replace(/\D/g, ''); // Remove non-digits
                if (value.length > 5) {
                    value = value.substring(0, 5) + '-' + value.substring(5, 8);
                }
                e.target.value = value;

                // Trigger mock fetch when full length reached
                if (value.length === 9) {
                    fetchMockAddress(value);
                } else {
                    // Hide address block if incomplete
                    addressDisplay.classList.add('hidden');
                    addressDisplay.classList.remove('flex');
                    cepStatus.classList.remove('opacity-100');
                }
            });

            function fetchMockAddress(cep) {
                // Show loading state
                cepStatus.textContent = 'Fetching...';
                cepStatus.classList.add('opacity-100');
                
                // Simulate network request (ViaCEP placeholder)
                setTimeout(() => {
                    // Mock data
                    addrStreet.textContent = 'Rua das Flores, 123';
                    addrNeighborhood.textContent = 'Bairro Botânico';
                    addrCityState.textContent = 'São Paulo - SP';
                    
                    cepStatus.textContent = 'Verified';
                    
                    // Show block
                    addressDisplay.classList.remove('hidden');
                    addressDisplay.classList.add('flex');
                    
                    // Fade out success message after a bit
                    setTimeout(() => {
                        cepStatus.classList.remove('opacity-100');
                    }, 2000);

                }, 800);
            }
        });
    </script>
</body></html>

<!-- Cadastro - DevCook -->
<!DOCTYPE html>

<html class="light" lang="en"><head>
<meta charset="utf-8"/>
<meta content="width=device-width, initial-scale=1.0" name="viewport"/>
<title>DevCook - Explore Recipes</title>
<script src="https://cdn.tailwindcss.com?plugins=forms,container-queries"></script>
<link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;600&amp;family=Epilogue:wght@600;700&amp;display=swap" rel="stylesheet"/>
<link href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:wght,FILL@100..700,0..1&amp;display=swap" rel="stylesheet"/>
<link href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:wght,FILL@100..700,0..1&amp;display=swap" rel="stylesheet"/>
<script id="tailwind-config">
        tailwind.config = {
            darkMode: "class",
            theme: {
                extend: {
                    colors: {
                        "secondary": "#006d37",
                        "on-error-container": "#93000a",
                        "on-primary-container": "#502600",
                        "on-surface-variant": "#564337",
                        "on-tertiary-fixed": "#2b1700",
                        "primary-container": "#e67e22",
                        "on-surface": "#091d2e",
                        "outline-variant": "#dcc1b1",
                        "surface-bright": "#f7f9ff",
                        "tertiary": "#865300",
                        "on-error": "#ffffff",
                        "on-secondary-fixed-variant": "#005228",
                        "primary-fixed-dim": "#ffb783",
                        "surface-container-high": "#d9eaff",
                        "on-secondary": "#ffffff",
                        "on-secondary-fixed": "#00210c",
                        "primary": "#944a00",
                        "on-secondary-container": "#007239",
                        "surface": "#f7f9ff",
                        "tertiary-fixed-dim": "#ffb961",
                        "secondary-container": "#7bf8a1",
                        "inverse-on-surface": "#e8f2ff",
                        "primary-fixed": "#ffdcc5",
                        "surface-container": "#e3efff",
                        "inverse-primary": "#ffb783",
                        "secondary-fixed": "#7efba4",
                        "error-container": "#ffdad6",
                        "on-tertiary-container": "#482b00",
                        "inverse-surface": "#203243",
                        "tertiary-fixed": "#ffddb9",
                        "on-tertiary": "#ffffff",
                        "surface-container-highest": "#d1e4fb",
                        "error": "#ba1a1a",
                        "surface-tint": "#944a00",
                        "on-primary-fixed": "#301400",
                        "secondary-fixed-dim": "#61de8a",
                        "surface-variant": "#d1e4fb",
                        "on-background": "#091d2e",
                        "tertiary-container": "#d78800",
                        "on-tertiary-fixed-variant": "#663e00",
                        "surface-container-low": "#edf4ff",
                        "background": "#f7f9ff",
                        "on-primary-fixed-variant": "#713700",
                        "surface-dim": "#c9dcf3",
                        "outline": "#897365",
                        "on-primary": "#ffffff",
                        "surface-container-lowest": "#ffffff"
                    },
                    borderRadius: {
                        "DEFAULT": "1rem",
                        "lg": "2rem",
                        "xl": "3rem",
                        "full": "9999px"
                    },
                    spacing: {
                        "sm": "12px",
                        "lg": "40px",
                        "margin-mobile": "16px",
                        "gutter": "24px",
                        "md": "24px",
                        "xs": "4px",
                        "xl": "64px",
                        "base": "8px",
                        "container-max": "1200px"
                    },
                    fontFamily: {
                        "headline-lg-mobile": ["Epilogue"],
                        "display-lg": ["Epilogue"],
                        "label-md": ["Plus Jakarta Sans"],
                        "headline-md": ["Epilogue"],
                        "caption": ["Plus Jakarta Sans"],
                        "body-md": ["Plus Jakarta Sans"],
                        "body-lg": ["Plus Jakarta Sans"],
                        "headline-lg": ["Epilogue"]
                    },
                    fontSize: {
                        "headline-lg-mobile": ["28px", { lineHeight: "36px", fontWeight: "600" }],
                        "display-lg": ["48px", { lineHeight: "56px", letterSpacing: "-0.02em", fontWeight: "700" }],
                        "label-md": ["14px", { lineHeight: "20px", letterSpacing: "0.01em", fontWeight: "600" }],
                        "headline-md": ["24px", { lineHeight: "32px", fontWeight: "600" }],
                        "caption": ["12px", { lineHeight: "16px", fontWeight: "500" }],
                        "body-md": ["16px", { lineHeight: "24px", fontWeight: "400" }],
                        "body-lg": ["18px", { lineHeight: "28px", fontWeight: "400" }],
                        "headline-lg": ["32px", { lineHeight: "40px", letterSpacing: "-0.01em", fontWeight: "600" }]
                    }
                }
            }
        }
    </script>
<style>
        .material-symbols-outlined {
            font-variation-settings: 'FILL' 0, 'wght' 400, 'GRAD' 0, 'opsz' 24;
        }
    </style>
</head>
<body class="bg-background text-on-background min-h-screen pb-24 md:pb-0">
<!-- Desktop Sidebar (NavigationDrawer) -->
<aside class="hidden md:flex flex-col h-full py-lg bg-surface dark:bg-inverse-surface shadow-xl h-full w-80 rounded-r-lg fixed left-0 top-0 z-50">
<div class="px-gutter mb-xl flex items-center justify-start gap-4">
<div class="w-12 h-12 rounded-full overflow-hidden bg-primary-container shrink-0">
<img class="w-full h-full object-cover" data-alt="Close-up portrait of a developer chef wearing an apron in a modern kitchen setting, bright soft lighting, high-end culinary photography aesthetic." src="https://lh3.googleusercontent.com/aida-public/AB6AXuDQm-CGjEsFFd5lK4wF6OklnxApqzHS8AA7MuHqJwV6mHiu6Y7hGeRZwTghqLa_Zi6e_liE4WhtcB_wlLWBph1LxuMQfd6UJ2A2F_E48WrzEbKpuG79SBYtiQ4zUpCknYdapzHEc41xr_w3xJ8mvzwsigOb_EBTyxyh50LDjq40jGNqSs6OcMsWp0LOAgeVthatLClKSW4twjolWAcfBD9k4S9cJiMdU__Aa_o4kj6zJIsXyrI2L0q1hg"/>
</div>
<div>
<h2 class="font-headline-md text-headline-md text-primary dark:text-primary-fixed-dim">Chef Developer</h2>
<p class="font-body-md text-body-md text-on-surface-variant">Mastering React &amp; Risotto</p>
</div>
</div>
<nav class="flex-1 px-4 space-y-2">
<a class="flex items-center gap-4 px-4 py-3 bg-primary-container text-on-primary-container font-bold rounded-full mx-2 translate-x-1 duration-150 shadow-sm cursor-pointer" href="#">
<span class="material-symbols-outlined" data-icon="search" style="font-variation-settings: 'FILL' 1;">search</span>
<span class="font-label-md text-label-md">Explore</span>
</a>
<a class="flex items-center gap-4 px-4 py-3 text-on-surface-variant hover:bg-surface-variant/50 rounded-full mx-2 transition-colors cursor-pointer hover:bg-surface-variant/30 dark:hover:bg-surface-container-high" href="#">
<span class="material-symbols-outlined" data-icon="favorite">favorite</span>
<span class="font-label-md text-label-md">My Recipes</span>
</a>
<a class="flex items-center gap-4 px-4 py-3 text-on-surface-variant hover:bg-surface-variant/50 rounded-full mx-2 transition-colors cursor-pointer hover:bg-surface-variant/30 dark:hover:bg-surface-container-high" href="#">
<span class="material-symbols-outlined" data-icon="add_box">add_box</span>
<span class="font-label-md text-label-md">Create New</span>
</a>
<a class="flex items-center gap-4 px-4 py-3 text-on-surface-variant hover:bg-surface-variant/50 rounded-full mx-2 transition-colors cursor-pointer hover:bg-surface-variant/30 dark:hover:bg-surface-container-high" href="#">
<span class="material-symbols-outlined" data-icon="settings">settings</span>
<span class="font-label-md text-label-md">Settings</span>
</a>
</nav>
</aside>
<!-- Main Content Area -->
<main class="md:ml-80 min-h-screen">
<!-- Mobile TopAppBar -->
<header class="md:hidden flex justify-between items-center w-full px-margin-mobile py-base z-50 docked full-width top-0 sticky backdrop-blur-md bg-surface/90 dark:bg-inverse-surface/90 shadow-sm transition-colors">
<button class="w-10 h-10 flex items-center justify-center text-on-surface-variant dark:text-outline-variant hover:bg-surface-variant/50 dark:hover:bg-on-surface-variant/20 rounded-full transition-colors cursor-pointer">
<span class="material-symbols-outlined" data-icon="menu">menu</span>
</button>
<h1 class="font-headline-lg-mobile text-headline-lg-mobile font-bold text-primary dark:text-primary-fixed-dim tracking-tight">DevCook</h1>
<button class="w-10 h-10 flex items-center justify-center text-on-surface-variant dark:text-outline-variant hover:bg-surface-variant/50 dark:hover:bg-on-surface-variant/20 rounded-full transition-colors cursor-pointer">
<span class="material-symbols-outlined" data-icon="search">search</span>
</button>
</header>
<div class="max-w-[container-max] mx-auto px-margin-mobile md:px-lg py-gutter pt-md">
<!-- Hero Search Section -->
<section class="mb-xl">
<h1 class="hidden md:block font-display-lg text-display-lg text-primary mb-gutter">Find your next culinary project.</h1>
<div class="relative w-full max-w-2xl group">
<div class="absolute inset-y-0 left-0 pl-6 flex items-center pointer-events-none text-on-surface-variant">
<span class="material-symbols-outlined text-2xl">search</span>
</div>
<input class="w-full pl-16 pr-6 py-4 bg-surface rounded-full border-none shadow-[0_4px_20px_rgba(0,0,0,0.05)] focus:ring-2 focus:ring-primary focus:shadow-[0_8px_32px_rgba(148,74,0,0.15)] font-body-lg text-body-lg text-on-surface placeholder:text-on-surface-variant/60 transition-all outline-none" placeholder="Search by ingredients (e.g., garlic, tomato, basil)..." type="text"/>
</div>
<!-- Category Filters (Bento-style layout on desktop, scroll on mobile) -->
<div class="mt-8 flex gap-sm overflow-x-auto pb-4 scrollbar-hide snap-x">
<button class="snap-start shrink-0 flex items-center gap-2 px-6 py-3 bg-secondary/10 text-secondary border border-secondary/20 rounded-full font-label-md text-label-md hover:bg-secondary/20 transition-colors shadow-sm">
<span class="material-symbols-outlined text-lg">restaurant</span>
                        Pasta
                    </button>
<button class="snap-start shrink-0 flex items-center gap-2 px-6 py-3 bg-surface text-on-surface-variant border border-outline-variant/50 rounded-full font-label-md text-label-md hover:bg-surface-variant/50 transition-colors shadow-sm">
<span class="material-symbols-outlined text-lg">icecream</span>
                        Desserts
                    </button>
<button class="snap-start shrink-0 flex items-center gap-2 px-6 py-3 bg-surface text-on-surface-variant border border-outline-variant/50 rounded-full font-label-md text-label-md hover:bg-surface-variant/50 transition-colors shadow-sm">
<span class="material-symbols-outlined text-lg">eco</span>
                        Vegan
                    </button>
<button class="snap-start shrink-0 flex items-center gap-2 px-6 py-3 bg-surface text-on-surface-variant border border-outline-variant/50 rounded-full font-label-md text-label-md hover:bg-surface-variant/50 transition-colors shadow-sm">
<span class="material-symbols-outlined text-lg">fitness_center</span>
                        Low-Carb
                    </button>
</div>
</section>
<!-- Recipe Grid -->
<section>
<div class="flex justify-between items-end mb-md">
<h2 class="font-headline-md text-headline-md text-on-surface">Trending Recipes</h2>
</div>
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-md">
<!-- Recipe Card 1 -->
<article class="group bg-surface rounded-lg shadow-[0_4px_20px_rgba(148,74,0,0.05)] hover:shadow-[0_8px_32px_rgba(148,74,0,0.08)] hover:-translate-y-1 transition-all duration-300 overflow-hidden cursor-pointer relative flex flex-col">
<button class="absolute top-4 right-4 z-10 w-10 h-10 bg-surface/80 backdrop-blur-md rounded-full flex items-center justify-center text-on-surface-variant hover:text-primary hover:bg-surface transition-colors shadow-sm">
<span class="material-symbols-outlined" data-icon="favorite">favorite</span>
</button>
<div class="aspect-video w-full overflow-hidden">
<img class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500" data-alt="A beautifully plated bowl of creamy carbonara pasta with crispy pancetta, black pepper, and a fresh egg yolk, shot from overhead in warm natural light on a rustic wooden table." src="https://lh3.googleusercontent.com/aida-public/AB6AXuBiDlzdR4JW0_hJeWlWLLya1cnlxcmhNLeDmn0nFRe0PZU8F2dnTxmdixTAIV2bB8z3_bbJ1CNsUcvkL-4wDGEsDJVlvhODwyVyd-eyFy7M2FU1vf2sGvW8PW9WB1bMy5Cs54qGYq43H0oooKOud_ax8qmDN2CCjwXkQG9uKRy6Wuh9JpohUDxFPjbV2cTgNTeS-uOnhrQjqmMlmDtHocSsdFQ55H0w_oV083aWJ4Ll5mDvEaVToyOEYA"/>
</div>
<div class="p-md flex-1 flex flex-col">
<h3 class="font-headline-md text-headline-md text-on-surface mb-2">Classic Roman Carbonara</h3>
<div class="flex gap-4 mt-auto pt-4 border-t border-outline-variant/20">
<div class="flex items-center gap-1 text-on-surface-variant font-caption text-caption">
<span class="material-symbols-outlined text-sm">schedule</span> 25m
                                </div>
<div class="flex items-center gap-1 text-on-surface-variant font-caption text-caption">
<span class="material-symbols-outlined text-sm">bolt</span> Easy
                                </div>
<div class="flex items-center gap-1 text-on-surface-variant font-caption text-caption ml-auto">
<span class="material-symbols-outlined text-sm text-primary">star</span> 4.9
                                </div>
</div>
</div>
</article>
<!-- Recipe Card 2 -->
<article class="group bg-surface rounded-lg shadow-[0_4px_20px_rgba(148,74,0,0.05)] hover:shadow-[0_8px_32px_rgba(148,74,0,0.08)] hover:-translate-y-1 transition-all duration-300 overflow-hidden cursor-pointer relative flex flex-col">
<button class="absolute top-4 right-4 z-10 w-10 h-10 bg-surface/80 backdrop-blur-md rounded-full flex items-center justify-center text-primary bg-surface transition-colors shadow-sm">
<span class="material-symbols-outlined" data-icon="favorite" style="font-variation-settings: 'FILL' 1;">favorite</span>
</button>
<div class="aspect-video w-full overflow-hidden">
<img class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500" data-alt="A vibrant vegan Buddha bowl filled with roasted sweet potatoes, quinoa, sliced avocado, fresh greens, and a tahini drizzle, bright colorful aesthetic on a modern white countertop." src="https://lh3.googleusercontent.com/aida-public/AB6AXuBnP8iVWFefyJfiihN7017gixPRFffZPMCzO-J5jDhSQoVN0pIWgRMJ1Vy27013q0W0hO0spr1w4na3MY2s7g-zQKaJTv5hl3obCq6eRCox8NQnKMZ4YNMDGpIY0C6j4lY4teA3EdvQZPeYV8DD2Il-_LOOnTAmaE2M9bevOeAeqFrLPoGaeLzVKobKbqviMj3H_JXMUdez_cFSm6iVohZmQtnEUxCj7SyQM7Q4Znb4SrLqMuAygkDC5w"/>
</div>
<div class="p-md flex-1 flex flex-col">
<h3 class="font-headline-md text-headline-md text-on-surface mb-2">Roasted Sweet Potato Bowl</h3>
<div class="flex gap-4 mt-auto pt-4 border-t border-outline-variant/20">
<div class="flex items-center gap-1 text-on-surface-variant font-caption text-caption">
<span class="material-symbols-outlined text-sm">schedule</span> 40m
                                </div>
<div class="flex items-center gap-1 text-on-surface-variant font-caption text-caption">
<span class="material-symbols-outlined text-sm">bolt</span> Medium
                                </div>
<div class="flex items-center gap-1 text-on-surface-variant font-caption text-caption ml-auto">
<span class="material-symbols-outlined text-sm text-primary">star</span> 4.7
                                </div>
</div>
</div>
</article>
<!-- Recipe Card 3 -->
<article class="group bg-surface rounded-lg shadow-[0_4px_20px_rgba(148,74,0,0.05)] hover:shadow-[0_8px_32px_rgba(148,74,0,0.08)] hover:-translate-y-1 transition-all duration-300 overflow-hidden cursor-pointer relative flex flex-col">
<button class="absolute top-4 right-4 z-10 w-10 h-10 bg-surface/80 backdrop-blur-md rounded-full flex items-center justify-center text-on-surface-variant hover:text-primary hover:bg-surface transition-colors shadow-sm">
<span class="material-symbols-outlined" data-icon="favorite">favorite</span>
</button>
<div class="aspect-video w-full overflow-hidden">
<img class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500" data-alt="A slice of rich dark chocolate tart with a glossy ganache finish, sprinkled with sea salt flakes, set on a dark moody slate background with soft dramatic lighting." src="https://lh3.googleusercontent.com/aida-public/AB6AXuCoOii7HJd-uyM55uU_bIGxH_4_5SKUEg6mHkSCPCMT6nlh0O3fhgFPV8rL2W6H2KiekgQq1m7JocdC1mk520gWMsqHixPHw532HHIgxXwOiy-9ZLPmq4siMOhc3mwydZfkzvmsWyyoKTWloB59Yo80NGkfhZ_ZKobhB4NF8p3dSQAfutezY32IF0P3Cqna08AOQZmVQgTECvAxOl6uI8IaWETuBss82lkghVgRNnpQBy3iL9O0_-Riqg"/>
</div>
<div class="p-md flex-1 flex flex-col">
<h3 class="font-headline-md text-headline-md text-on-surface mb-2">Sea Salt Chocolate Tart</h3>
<div class="flex gap-4 mt-auto pt-4 border-t border-outline-variant/20">
<div class="flex items-center gap-1 text-on-surface-variant font-caption text-caption">
<span class="material-symbols-outlined text-sm">schedule</span> 1h 20m
                                </div>
<div class="flex items-center gap-1 text-on-surface-variant font-caption text-caption">
<span class="material-symbols-outlined text-sm">bolt</span> Hard
                                </div>
<div class="flex items-center gap-1 text-on-surface-variant font-caption text-caption ml-auto">
<span class="material-symbols-outlined text-sm text-primary">star</span> 5.0
                                </div>
</div>
</div>
</article>
</div>
</section>
<!-- Empty State Placeholder (Hidden by default, shown for demonstration logic) -->
<section class="hidden flex-col items-center justify-center py-xl mt-lg text-center bg-surface-container-low rounded-lg border-2 border-dashed border-outline-variant/30">
<span class="material-symbols-outlined text-6xl text-outline mb-4">search_off</span>
<h3 class="font-headline-md text-headline-md text-on-surface mb-2">No recipes found</h3>
<p class="font-body-md text-body-md text-on-surface-variant max-w-sm mb-6">We couldn't find any recipes matching your ingredients. Try adjusting your search or exploring our categories.</p>
<button class="px-6 py-3 bg-primary text-on-primary rounded-full font-label-md text-label-md hover:bg-primary-container hover:text-on-primary-container transition-colors shadow-sm">
                    Clear Search
                </button>
</section>
</div>
</main>
<!-- Mobile BottomNavBar -->
<nav class="md:hidden fixed bottom-0 left-0 w-full z-50 flex justify-around items-center px-4 py-2 pb-safe backdrop-blur-md bg-surface/90 dark:bg-inverse-surface/90 border-t border-outline-variant/30 shadow-[0_-4px_20px_rgba(0,0,0,0.05)] rounded-t-lg">
<a class="flex flex-col items-center justify-center text-primary dark:text-primary-fixed-dim font-bold bg-primary-fixed/20 rounded-xl px-4 py-2 scale-90 duration-200 cursor-pointer hover:bg-surface-container-high/50 dark:hover:bg-surface-container-highest/20 transition-all" href="#">
<span class="material-symbols-outlined" data-icon="explore" style="font-variation-settings: 'FILL' 1;">explore</span>
<span class="font-label-md text-label-md-mobile mt-1">Explore</span>
</a>
<a class="flex flex-col items-center justify-center text-on-surface-variant dark:text-outline-variant px-4 py-2 cursor-pointer hover:bg-surface-container-high/50 dark:hover:bg-surface-container-highest/20 transition-all" href="#">
<span class="material-symbols-outlined" data-icon="book">book</span>
<span class="font-label-md text-label-md-mobile mt-1">Recipes</span>
</a>
<a class="flex flex-col items-center justify-center text-on-surface-variant dark:text-outline-variant px-4 py-2 cursor-pointer hover:bg-surface-container-high/50 dark:hover:bg-surface-container-highest/20 transition-all" href="#">
<span class="material-symbols-outlined" data-icon="add_circle">add_circle</span>
<span class="font-label-md text-label-md-mobile mt-1">Create</span>
</a>
<a class="flex flex-col items-center justify-center text-on-surface-variant dark:text-outline-variant px-4 py-2 cursor-pointer hover:bg-surface-container-high/50 dark:hover:bg-surface-container-highest/20 transition-all" href="#">
<span class="material-symbols-outlined" data-icon="person">person</span>
<span class="font-label-md text-label-md-mobile mt-1">Profile</span>
</a>
</nav>
</body></html>
