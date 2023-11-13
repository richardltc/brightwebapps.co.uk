<script>
    import Step from "./Step.svelte";

    let steps = [
        {
            name: "Wynford Industrial Park",
            icon: "fa-solid fa-building",
            description:
                "Smoljames Store is a a merchanising store created with Next.js, Commerce.js & Stripe! Commerce.js is a CMS for managing project and Stripe is used for all transaction handling.",
        },
        {
            name: "BT Architect",
            icon: "fa-solid fa-house",
            description:
                "Brian Turner R.I.B.A. is a chartered and registered Architect and a member of the Royal Institute of British Architects.\n",
        },
        {
            name: "Wynford Caravan Storage",
            icon: "fa-solid fa-caravan",
            description:
                "Situated on land adjacent to Wynford Industrial Park the facility is surrounded with a security fence and a protective, landscaped earth bund.",
        },
    ];

    let benefits = [
        {
            metric: "10x",
            name: "Richard",
            description:
                "Richard started coding back in the 90's writing Windows client/server business applications using Borland Delphi.  " +
                "Since then, Richard has always had a focus on writing fast and solid applications" +
                " and favours the fast full-stack web framework SvelteKit for building modern web applications. He also enjoys DevOps",
        },
        {
            name: "a product design & UX fanatic",
            description:
                "We carefully craft and designing amazing user experiences, with a focus on speed and a mobile first approach.",
        },
        {
            name: "excellent communicators",
            description:
                "Communication is key and it's a paramount value of ours. We believe in transparency and constructive " +
                "communication above all else. This helps us develop deep relationships and ensures our effectiveness " +
                "and productivity in any work space with any team.",
        },
    ];
</script>

<main class="flex flex-col flex-1 p-4">
    <section
            id="introPage"
            class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14"
    >
        <div
                class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10"
        >
            <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
                Hi! We're <span class="poppins text-violet-400">Bright</span> Web Apps
                <br />Full Stack
                <span class="poppins text-violet-400">Developers</span>
            </h2>
            <p class="text-base sm:text-lg md:text-xl">
                If you need a <span class="text-violet-400">full stack</span> web application, or a performant
                <span class="text-violet-400">web site</span> we can build it for you!
            </p>
            <button
                    class="blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950"
            >
                <div
                        class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"
                />
                <h4 class="relative z-9">Get in touch &rarr;</h4>
            </button>
        </div>
    </section>
    <section class="py-20 lg:py-32 flex flex-col gap-24" id="projects">
        <div class="flex flex-col gap-2 text-center">
            <h6 class="text-large sm:text-xl md:text-2xl">
                A few of our sites.
            </h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                Curious to <span class="poppins text-violet-400">see</span> our work?
            </h3>
        </div>
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
            <Step step={steps[0]}>
                <p>
                    <strong class="text-violet-400">Wynford Industrial Park</strong>
                     is home to a thriving Romsey business community.
                    We strive to offer the very best in flexibility and support to our tenants to assist in the success of their business.<strong
                        class="text-violet-400"></p>
            </Step>
            <Step step={steps[1]}>
                <p>
                    <strong
                        class="text-violet-400">BT Architect</strong
                >,
                    Brian Turner R.I.B.A. is a chartered and registered Architect and a member of the Royal Institute of British Architects.
                    He has a worked as an Architect running his own practice for over 20 years.
                </p>
            </Step>
            <Step step={steps[2]}>
                <p>
                    Wynford <strong class="text-violet-400"
                >Caravan Storage</strong
                >
                    Situated on land adjacent to Wynford Industrial Park the facility is surrounded with a security fence and a protective, landscaped earth bund.
                    Access is available 24/7 by a double set of card controlled electric security gates.
                    All movements and the storage area monitored by security cameras placed around the site.
                </p>
            </Step>
        </div>
    </section>
    <section
            id="about"
            class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative"
    >
        <!-- <div class="z-[-1] bg-violet-950 w-screen left-1/2 -translate-x-1/2 top-0 h-full absolute"> </div> -->
        <div
                class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-4"
        >
            <h6 class="text-large sm:text-xl md:text-2xl">
                Want to know more?
            </h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                A bit <span class="poppins text-violet-400">about</span> us.
            </h3>
        </div>
        <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">
            We are . . .
        </p>
        <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
            {#each benefits as benefit, index}
                <div class="flex gap-6 sm:gap-8">
                    <p
                            class="poppins text-4xl sm:text-5xl md:text-6xl text-slate-500 font-semibold"
                    >
                        0{index + 1}
                    </p>
                    <div class="flex flex-col gap-6 sm:gap-8">
                        <h3 class="text-2xl sm:text-3xl md:text-5xl">
                            {benefit.name}
                        </h3>
                        <p>{benefit.description}</p>
                    </div>
                </div>
            {/each}
        </div>
    </section>
</main>