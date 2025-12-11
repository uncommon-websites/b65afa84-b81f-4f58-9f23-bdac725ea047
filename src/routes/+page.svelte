<script lang="ts">
	import { onMount } from 'svelte';

    // Trusted by leading defense contractors and regulated firms
    const partners = [
        { name: 'Lockheed Martin', src: 'https://placehold.co/80x30?text=Lockheed' },
        { name: 'Raytheon', src: 'https://placehold.co/80x30?text=Raytheon' },
        { name: 'Northrop Grumman', src: 'https://placehold.co/80x30?text=Northrop' },
        { name: 'BAE Systems', src: 'https://placehold.co/80x30?text=BAE' },
        { name: 'Booz Allen', src: 'https://placehold.co/80x30?text=BoozAllen' },
        { name: 'Palantir', src: 'https://placehold.co/80x30?text=Palantir' },
        { name: 'Leidos', src: 'https://placehold.co/80x30?text=Leidos' },
        { name: 'SAIC', src: 'https://placehold.co/80x30?text=SAIC' },
        { name: 'General Dynamics', src: 'https://placehold.co/80x30?text=GDIT' },
        { name: 'CACI', src: 'https://placehold.co/80x30?text=CACI' },
        { name: 'ManTech', src: 'https://placehold.co/80x30?text=ManTech' },
        { name: 'Peraton', src: 'https://placehold.co/80x30?text=Peraton' },
        { name: 'Parsons', src: 'https://placehold.co/80x30?text=Parsons' },
        { name: 'L3Harris', src: 'https://placehold.co/80x30?text=L3Harris' },
        { name: 'Kratos', src: 'https://placehold.co/80x30?text=Kratos' },
        { name: 'Cubic', src: 'https://placehold.co/80x30?text=Cubic' },
        { name: 'DXC Technology', src: 'https://placehold.co/80x30?text=DXC' },
        { name: 'Accenture Federal', src: 'https://placehold.co/80x30?text=Accenture' },
        { name: 'Deloitte', src: 'https://placehold.co/80x30?text=Deloitte' },
        { name: 'KPMG', src: 'https://placehold.co/80x30?text=KPMG' },
        { name: 'PwC', src: 'https://placehold.co/80x30?text=PwC' },
    ];

    const articles = [
        {
            tag: 'Case Study',
            title: 'Defense Contractor Achieves 100% Audit Readiness',
            desc: 'How a leading defense contractor reduced compliance preparation time from weeks to hours with automated evidence tracking.',
            img: 'https://placehold.co/300x200/E8E8E3/1a1a1a?text=Defense',
            bg: 'bg-gray-100'
        },
        {
            tag: 'White Paper',
            title: 'The Future of Threat Intelligence',
            desc: 'Advanced NLP and machine learning techniques for extracting actionable intelligence from unstructured data sources.',
            img: 'https://placehold.co/300x200/D4C5A3/1a1a1a?text=Threat',
            bg: 'bg-primary-50'
        },
        {
            tag: 'Research',
            title: 'Real-Time Compliance Monitoring',
            desc: 'How continuous monitoring dashboards are transforming vendor risk management in the $50B cybersecurity market.',
            img: 'https://placehold.co/300x200/E8E8E3/1a1a1a?text=Compliance',
            bg: 'bg-gray-100'
        },
        {
            tag: 'Industry Report',
            title: 'Supply Chain Security in 2025',
            desc: 'Insights from leading procurement teams on overcoming vendor risk concerns with real-time intelligence.',
            img: 'https://placehold.co/300x200/F0E6D2/1a1a1a?text=Supply',
            bg: 'bg-primary-50'
        }
    ];

    const testimonials = [
        {
            quote: "Centinel Analytica transformed our compliance process. What used to take weeks now takes hours. The centralized evidence tracking is a game-changer.",
            author: "Sarah Mitchell",
            role: "Chief Compliance Officer",
            company: "Leading Defense Contractor",
            img: "/generated/image-professional-compliance-officer-in-busin-1765467903052-1.webp"
        }
    ];
</script>

<div class="min-h-screen bg-white text-gray-900 font-sans selection:bg-gray-200">
    <!-- Header -->
    <header class="fixed top-0 left-0 right-0 z-50 bg-white/90 backdrop-blur-sm border-b border-gray-100">
        <div class="max-w-[1600px] mx-auto px-6 py-6 flex justify-between items-center">
            <div class="flex items-center gap-3">
                <svg class="w-8 h-8 text-primary-600" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path
                        fill-rule="evenodd"
                        clip-rule="evenodd"
                        d="M6.99251 12.196C6.85314 12.5757 6.62925 12.9208 6.33682 13.2067H6.33835C6.00191 13.5351 5.58566 13.7756 5.12816 13.9059C4.67065 14.0362 4.18671 14.0522 3.72118 13.9523C3.25564 13.8524 2.82357 13.64 2.46501 13.3345C2.10645 13.0291 1.83299 12.6406 1.66998 12.2051C1.50697 11.7696 1.45969 11.3012 1.5325 10.8432C1.60532 10.3852 1.79587 9.95244 2.08653 9.58516C2.37718 9.21781 2.75852 8.9277 3.1952 8.74177C3.63188 8.55585 4.10979 8.48002 4.58462 8.52142L4.57074 8.50792C5.0567 8.54782 5.54575 8.48407 6.00378 8.32124C6.4618 8.15846 6.87776 7.90043 7.2226 7.56521C7.56746 7.22998 7.83285 6.82564 8.00036 6.38041C8.16786 5.93517 8.23344 5.45976 8.1924 4.98737L8.20628 5.00087C8.15181 4.43594 8.27796 3.86844 8.56753 3.37575C8.85701 2.88307 9.29579 2.48919 9.82407 2.24782C10.3523 2.00645 10.9443 1.92933 11.5192 2.02701C12.0942 2.12467 12.6243 2.39237 13.037 2.79358C13.4497 3.19479 13.7251 3.70999 13.8256 4.26892C13.926 4.82785 13.8467 5.4033 13.5984 5.9168C13.3501 6.4303 12.9449 6.85685 12.4381 7.13828C11.9313 7.41971 11.3474 7.54233 10.7663 7.4894L10.781 7.5029C10.2949 7.46279 9.80563 7.52632 9.34741 7.68904C8.88919 7.85176 8.47309 8.10975 8.12805 8.44499C7.78301 8.78025 7.51742 9.18466 7.34983 9.63001C7.18224 10.0754 7.11669 10.551 7.15774 11.0235L7.14309 11.01C7.1833 11.4112 7.13189 11.8162 6.99251 12.196ZM11.5077 14.7121L11.493 14.6986C11.9061 14.739 12.3232 14.6897 12.7143 14.5543C13.1053 14.4188 13.4605 14.2007 13.7542 13.9154C14.0477 13.6302 14.2726 13.285 14.4121 12.905C14.5518 12.525 14.6028 12.1196 14.5615 11.718L14.5762 11.7315C14.5351 11.2591 14.6007 10.7838 14.7681 10.3385C14.9356 9.89327 15.2011 9.48893 15.5459 9.15368C15.8908 8.8185 16.3068 8.56042 16.7648 8.39767C17.2228 8.23481 17.7118 8.17111 18.1978 8.21099L18.1832 8.19749C18.7645 8.25059 19.3485 8.12801 19.8556 7.84656C20.3627 7.56511 20.7681 7.13845 21.0165 6.62479C21.265 6.11114 21.3444 5.53548 21.2439 4.97634C21.1435 4.4172 20.868 3.9018 20.4551 3.50044C20.0422 3.09909 19.512 2.8313 18.9368 2.73364C18.3616 2.63596 17.7695 2.71315 17.241 2.95467C16.7126 3.19618 16.2737 3.59027 15.9842 4.08319C15.6946 4.57609 15.5685 5.14383 15.6232 5.70895L15.6093 5.6947C15.6504 6.16712 15.585 6.64259 15.4175 7.08788C15.2501 7.53318 14.9846 7.93758 14.6398 8.27287C14.2949 8.60805 13.8789 8.86612 13.4208 9.02888C12.9627 9.19163 12.4736 9.25523 11.9876 9.21526L12.0015 9.22951C11.5885 9.18908 11.1713 9.23836 10.7803 9.37381C10.3893 9.50919 10.034 9.72744 9.74039 10.0127C9.44674 10.2979 9.22199 10.6431 9.08234 11.0231C8.94276 11.4031 8.89176 11.8085 8.93304 12.2101L8.91915 12.1966C8.96005 12.6689 8.89439 13.1443 8.72688 13.5895C8.5593 14.0346 8.29389 14.4389 7.94908 14.7741C7.60425 15.1093 7.18835 15.3673 6.73039 15.5302C6.27242 15.693 5.78342 15.7569 5.29749 15.7171L5.31138 15.7306C4.73003 15.6775 4.14599 15.8001 3.63892 16.0815C3.13186 16.363 2.72644 16.7896 2.478 17.3033C2.22954 17.817 2.15013 18.3926 2.25061 18.9518C2.35109 19.5109 2.62657 20.0263 3.03945 20.4276C3.45234 20.829 3.98253 21.0968 4.55773 21.1944C5.13293 21.2921 5.72512 21.2149 6.25353 20.9734C6.78193 20.7319 7.22085 20.3379 7.51038 19.8449C7.79994 19.352 7.92601 18.7843 7.87139 18.2191L7.88605 18.2326C7.845 17.7602 7.91058 17.2849 8.07809 16.8396C8.24551 16.3944 8.511 15.99 8.85581 15.6548C9.20069 15.3196 9.61664 15.0615 10.0746 14.8988C10.5327 14.7359 11.0217 14.6722 11.5077 14.7121ZM17.1996 10.7633C16.9071 11.0493 16.6832 11.3944 16.5437 11.7741C16.4042 12.1538 16.3526 12.5587 16.3925 12.9601L16.3786 12.9466C16.4197 13.419 16.3541 13.8944 16.1866 14.3396C16.0191 14.7849 15.7537 15.1892 15.4089 15.5244C15.064 15.8596 14.648 16.1177 14.19 16.2804C13.732 16.4433 13.2429 16.507 12.757 16.4671L12.7708 16.4806C12.1896 16.4281 11.6057 16.551 11.0989 16.8328C10.5921 17.1145 10.1871 17.5414 9.93902 18.0551C9.69097 18.5689 9.61188 19.1444 9.71265 19.7035C9.81349 20.2625 10.0892 20.7777 10.5022 21.1788C10.9152 21.5799 11.4454 21.8474 12.0205 21.9448C12.5957 22.0423 13.1877 21.9649 13.716 21.7234C14.2443 21.4817 14.683 21.0877 14.9724 20.5947C15.2618 20.1018 15.3878 19.5342 15.3332 18.9692L15.3478 18.9827C15.3068 18.5103 15.3723 18.0349 15.5398 17.5896C15.7073 17.1444 15.9728 16.7401 16.3176 16.4048C16.6625 16.0696 17.0784 15.8115 17.5364 15.6488C17.9945 15.486 18.4835 15.4222 18.9695 15.4621L18.9548 15.4486C19.4296 15.4901 19.9076 15.4144 20.3444 15.2286C20.7811 15.0427 21.1625 14.7527 21.4533 14.3854C21.744 14.0181 21.9347 13.5854 22.0075 13.1274C22.0805 12.6694 22.0332 12.2009 21.8703 11.7653C21.7073 11.3298 21.4339 10.9413 21.0754 10.6358C20.7168 10.3303 20.2848 10.1178 19.8192 10.0179C19.3536 9.91795 18.8697 9.93385 18.4121 10.0641C17.9546 10.1945 17.5383 10.4349 17.2019 10.7633H17.1996Z"
                        fill="currentColor"
                    />
                </svg>
                <a href="/" class="text-base font-semibold text-gray-900">
                    Centinel Analytica
                </a>
            </div>
            <div>
                <a href="#" class="bg-gray-900 text-white px-5 py-2.5 text-xs font-medium rounded-sm hover:bg-gray-800 transition-colors">
                    Request a Demo
                </a>
            </div>
        </div>
    </header>

    <main class="pt-32 pb-20">
        <div class="max-w-[1600px] mx-auto px-6 grid grid-cols-12 gap-8">
            <!-- Sidebar Navigation -->
            <div class="col-span-2 hidden lg:block sticky top-32 h-fit">
                <nav class="flex flex-col space-y-3 text-xs text-gray-500 font-medium">
                    <a href="#" class="text-gray-900">Home</a>
                    <a href="#" class="hover:text-gray-900 transition-colors">Platform</a>
                    <a href="#" class="hover:text-gray-900 transition-colors">Intelligence</a>
                    <a href="#" class="hover:text-gray-900 transition-colors">Resources</a>
                    <a href="#" class="hover:text-gray-900 transition-colors">Contact</a>
                </nav>
            </div>

            <!-- Main Content Area -->
            <div class="col-span-12 lg:col-span-10 space-y-32">
                
                <!-- Hero Section -->
                <section class="relative">
                    <div class="relative w-full h-[600px] overflow-hidden rounded-sm">
                        <!-- Cybersecurity Operations Center Background -->
                        <img src="/generated/image-cybersecurity-operations-center-with-mul-1765467899709-0.webp" alt="Cybersecurity operations center" class="absolute inset-0 w-full h-full object-cover" />
                        <div class="absolute inset-0 bg-gradient-to-b from-black/40 via-black/20 to-black/60"></div>
                        
                        <div class="absolute inset-0 flex flex-col items-center justify-center p-12 text-center">
                            <h1 class="text-4xl md:text-5xl font-normal text-white mb-12 max-w-3xl leading-tight">
                                Actionable intelligence from unstructured data<br>for defense and compliance
                            </h1>

                            <!-- Logos Card -->
                            <div class="bg-white/95 backdrop-blur-sm p-8 rounded-sm shadow-sm max-w-4xl w-full">
                                <p class="text-[10px] text-gray-500 mb-6 uppercase tracking-wide">
                                    Trusted by leading defense contractors and regulated firms for real-time threat intelligence and compliance monitoring.
                                </p>
                                <div class="grid grid-cols-4 md:grid-cols-7 gap-8 items-center justify-items-center opacity-80 grayscale">
                                    {#each partners as partner}
                                        <div class="h-6 flex items-center justify-center">
                                            <span class="text-[10px] font-bold text-gray-800">{partner.name}</span>
                                        </div>
                                    {/each}
                                </div>
                            </div>
                        </div>
                    </div>
                </section>

                <!-- How Centinel Works Section -->
                <section>
                    <div class="flex justify-between items-baseline mb-24 border-b border-gray-100 pb-4">
                        <h2 class="text-3xl font-light text-gray-900 max-w-xl leading-tight">
                            How Centinel transforms unstructured data into actionable intelligence
                        </h2>
                        <span class="text-[10px] text-gray-400 uppercase tracking-wider">Our Platform</span>
                    </div>

                    <div class="relative min-h-[800px]">
                        <!-- Diagram (Sticky/Fixed positioning simulation) -->
                        <div class="absolute right-0 top-0 w-1/2 p-8 bg-gray-50 rounded-sm">
                            <div class="text-[10px] text-gray-500 mb-4">Intelligence Pipeline</div>
                            <div class="flex items-center justify-between gap-4">
                                <div class="w-32 h-32 bg-gray-900 text-white flex flex-col items-center justify-center p-4 rounded-sm">
                                    <div class="mb-2">
                                        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12h6m-6 4h6m2 5H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z"></path></svg>
                                    </div>
                                    <span class="text-[10px] uppercase tracking-wider text-center">Unstructured Data</span>
                                </div>
                                
                                <div class="flex-1 h-32 bg-primary-50 border border-primary-200 rounded-sm flex flex-col items-center justify-center relative">
                                    <span class="text-[10px] text-gray-500 uppercase absolute top-2 left-4">NLP & ML Processing</span>
                                    <div class="w-full border-t border-dashed border-primary-300 absolute top-1/2"></div>
                                    
                                    <!-- Processing Icon -->
                                    <div class="absolute -bottom-6 bg-white border border-primary-200 p-2 shadow-sm rounded-sm flex items-center gap-2">
                                        <div class="w-8 h-10 border border-primary-300 flex items-center justify-center bg-primary-50">
                                            <svg class="w-4 h-4 text-primary-600" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z"></path></svg>
                                        </div>
                                        <div class="text-[8px] leading-tight text-gray-500">
                                            ADVANCED<br>ALGORITHMS
                                        </div>
                                    </div>
                                </div>

                                <div class="w-32 h-32 bg-gradient-to-br from-primary-600 to-primary-700 text-white flex flex-col items-center justify-center p-4 rounded-sm">
                                    <div class="mb-2">
                                        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 19v-6a2 2 0 00-2-2H5a2 2 0 00-2 2v6a2 2 0 002 2h2a2 2 0 002-2zm0 0V9a2 2 0 012-2h2a2 2 0 012 2v10m-6 0a2 2 0 002 2h2a2 2 0 002-2m0 0V5a2 2 0 012-2h2a2 2 0 012 2v14a2 2 0 01-2 2h-2a2 2 0 01-2-2z"></path></svg>
                                    </div>
                                    <span class="text-[10px] uppercase tracking-wider text-center">Actionable Intelligence</span>
                                </div>
                            </div>
                        </div>

                        <!-- Text Blocks -->
                        <div class="absolute left-0 top-[400px] max-w-xs">
                            <div class="flex gap-4">
                                <span class="bg-gray-900 text-white w-5 h-5 flex items-center justify-center text-xs font-medium shrink-0 rounded-sm">1</span>
                                <p class="text-sm text-gray-600 leading-relaxed">
                                    Centinel ingests unstructured data from multiple sources including threat feeds, security logs, and compliance documents.
                                </p>
                            </div>
                        </div>

                        <div class="absolute left-0 top-[600px] max-w-xs">
                            <div class="flex gap-4">
                                <span class="bg-gray-900 text-white w-5 h-5 flex items-center justify-center text-xs font-medium shrink-0 rounded-sm">2</span>
                                <p class="text-sm text-gray-600 leading-relaxed">
                                    Advanced NLP and machine learning algorithms extract patterns, threats, and compliance evidence in real-time.
                                </p>
                            </div>
                        </div>
                    </div>
                </section>

                <!-- Intelligence for Defense & Compliance Section -->
                <section>
                    <div class="flex justify-between items-baseline mb-16 border-b border-gray-100 pb-4">
                        <h2 class="text-3xl font-light text-gray-900">
                            Intelligence infrastructure for the modern threat landscape
                        </h2>
                        <span class="text-[10px] text-gray-400 uppercase tracking-wider">About Centinel</span>
                    </div>

                    <div class="grid grid-cols-1 md:grid-cols-3 gap-12 text-sm leading-relaxed text-gray-600 mb-24">
                        <p>
                            We are a threat intelligence and compliance platform serving defense contractors and regulated firms in the $50B cybersecurity market.
                        </p>
                        <div class="space-y-6">
                            <p>
                                In today's threat landscape, organizations are drowning in unstructured data. Security logs, threat feeds, compliance documents, and vendor assessments create an overwhelming volume of information that traditional tools struggle to process effectively.
                            </p>
                            <p>
                                Compliance officers at regulated firms face an impossible challenge: maintaining audit readiness without centralized evidence tracking. Procurement teams struggle with vendor risk assessments. Security leaders need real-time threat intelligence, not yesterday's reports.
                            </p>
                        </div>
                        <div class="space-y-6">
                            <p>
                                Centinel Analytica solves this with advanced natural language processing and machine learning algorithms that transform unstructured data into actionable intelligence. Our platform provides real-time compliance monitoring dashboards, automated evidence tracking, and classified threat intelligence at scale.
                            </p>
                            <p>
                                From defense contractors to financial institutions, we're helping organizations move from reactive compliance to proactive security posture management. Starting with 10K deployments, we're building the intelligence infrastructure for the next generation of cybersecurity.
                            </p>
                        </div>
                    </div>

                    <!-- Industry Recognition -->
                    <div class="bg-gray-50 rounded-sm p-8 flex items-center justify-between">
                        <span class="text-[10px] text-gray-400 uppercase tracking-wider mr-8">Industry Recognition :</span>
                        <div class="flex-1 flex justify-between items-center opacity-60 grayscale">
                            <span class="font-sans text-lg font-bold">Defense Tech Summit</span>
                            <span class="font-sans text-lg font-bold">RSA Conference</span>
                            <span class="font-serif text-lg">Cybersecurity Ventures</span>
                            <span class="font-serif text-lg">DARK READING</span>
                            <span class="font-serif text-lg">SC MEDIA</span>
                        </div>
                    </div>
                </section>

                <!-- Real-Time Intelligence Dashboard Section -->
                <section class="bg-gray-950 text-white rounded-sm overflow-hidden relative min-h-[400px] flex items-center">
                    <!-- Background Graphic -->
                    <div class="absolute inset-0 opacity-20">
                        <div class="absolute bottom-0 left-0 right-0 h-64 bg-gradient-to-t from-primary-900/50 to-transparent"></div>
                         <!-- Abstract network/data visualization -->
                        <svg class="absolute bottom-0 w-full h-full text-primary-900/30" viewBox="0 0 100 100" preserveAspectRatio="none">
                            <path d="M0 100 Q 50 50 100 100" fill="none" stroke="currentColor" stroke-width="0.5" />
                            <path d="M0 100 Q 50 40 100 100" fill="none" stroke="currentColor" stroke-width="0.5" />
                            <path d="M0 100 Q 50 30 100 100" fill="none" stroke="currentColor" stroke-width="0.5" />
                            <circle cx="20" cy="80" r="2" fill="currentColor" opacity="0.6" />
                            <circle cx="50" cy="60" r="2" fill="currentColor" opacity="0.6" />
                            <circle cx="80" cy="75" r="2" fill="currentColor" opacity="0.6" />
                        </svg>
                    </div>

                    <div class="relative z-10 p-16 w-full grid grid-cols-1 md:grid-cols-2 gap-12 items-center">
                        <div>
                            <h2 class="text-3xl font-light mb-6">
                                Real-time compliance monitoring<br>for audit readiness
                            </h2>
                            <p class="text-sm text-gray-400 mb-8 max-w-md">
                                Automated evidence tracking, vendor risk assessment, and threat intelligence in a unified dashboard. From weeks to hours.
                            </p>
                            <button class="bg-white text-gray-900 px-6 py-2 text-xs font-medium rounded-sm hover:bg-gray-200 transition-colors">
                                Explore Platform
                            </button>
                        </div>
                        <div class="flex justify-end">
                            <div class="w-64 h-80 bg-gradient-to-br from-primary-600/20 to-primary-800/20 rounded-lg p-1 shadow-2xl rotate-2 transform hover:rotate-0 transition-transform duration-500 border border-primary-500/30">
                                <div class="w-full h-full bg-gray-900/90 backdrop-blur-md border border-primary-500/20 rounded flex flex-col p-6 gap-4">
                                    <!-- Dashboard mockup -->
                                    <div class="flex items-center justify-between">
                                        <div class="text-[10px] uppercase tracking-wider text-primary-400">Live Dashboard</div>
                                        <div class="w-2 h-2 rounded-full bg-primary-400 animate-pulse"></div>
                                    </div>
                                    <div class="space-y-3 flex-1">
                                        <div class="h-12 bg-primary-500/10 rounded border border-primary-500/20 flex items-center px-3">
                                            <div class="w-full h-2 bg-primary-500/30 rounded"></div>
                                        </div>
                                        <div class="h-12 bg-primary-500/10 rounded border border-primary-500/20 flex items-center px-3">
                                            <div class="w-3/4 h-2 bg-primary-500/30 rounded"></div>
                                        </div>
                                        <div class="h-12 bg-primary-500/10 rounded border border-primary-500/20 flex items-center px-3">
                                            <div class="w-5/6 h-2 bg-primary-500/30 rounded"></div>
                                        </div>
                                    </div>
                                    <div class="grid grid-cols-3 gap-2">
                                        <div class="h-8 bg-primary-500/5 rounded border border-primary-500/10"></div>
                                        <div class="h-8 bg-primary-500/5 rounded border border-primary-500/10"></div>
                                        <div class="h-8 bg-primary-500/5 rounded border border-primary-500/10"></div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </section>

                <!-- Testimonials -->
                <section>
                    <div class="flex justify-between items-baseline mb-16 border-b border-gray-100 pb-4">
                        <h2 class="text-3xl font-light text-gray-900">
                            Trusted by compliance leaders
                        </h2>
                        <span class="text-[10px] text-gray-400 uppercase tracking-wider">Testimonials</span>
                    </div>

                    <div class="relative">
                        <div class="flex gap-8 overflow-hidden">
                            <div class="w-full md:w-[800px] shrink-0 bg-gray-50 flex">
                                <div class="w-1/3 shrink-0">
                                    <img src="/generated/image-professional-compliance-officer-in-busin-1765467903052-1.webp" alt="Sarah Mitchell" class="w-full h-full object-cover" />
                                </div>
                                <div class="w-2/3 p-12 flex flex-col justify-center">
                                    <blockquote class="text-xl font-light leading-relaxed mb-8">
                                        "Centinel Analytica transformed our compliance process. What used to take weeks now takes hours. The centralized evidence tracking is a game-changer."
                                    </blockquote>
                                    <div class="flex items-center gap-2 mb-2">
                                        <div class="w-1 h-8 bg-primary-500 rounded-full"></div>
                                        <span class="text-xs font-semibold text-gray-500">Leading Defense Contractor</span>
                                    </div>
                                    <div>
                                        <div class="font-medium">Sarah Mitchell</div>
                                        <div class="text-xs text-gray-500">Chief Compliance Officer</div>
                                    </div>
                                </div>
                            </div>
                            <!-- Next slide preview -->
                            <div class="w-1/3 shrink-0 opacity-50 bg-gray-100">
                                <div class="w-full h-full flex items-center justify-center text-gray-400">
                                    <svg class="w-12 h-12" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z"></path></svg>
                                </div>
                            </div>
                        </div>
                        
                        <!-- Navigation Button -->
                        <button class="absolute top-0 right-0 -mt-12 w-8 h-8 bg-gray-900 text-white flex items-center justify-center hover:bg-gray-800 transition-colors">
                            <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"></path></svg>
                        </button>
                    </div>
                </section>

                <!-- Read More / Articles -->
                <section>
                    <div class="flex justify-between items-baseline mb-16 border-b border-gray-100 pb-4">
                        <h2 class="text-3xl font-light text-gray-900">
                            Read more
                        </h2>
                        <span class="text-[10px] text-gray-400 uppercase tracking-wider">Articles</span>
                    </div>

                    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
                        {#each articles as article}
                            <div class="group cursor-pointer">
                                <div class="relative aspect-square mb-6 overflow-hidden {article.bg} flex items-center justify-center">
                                    <span class="absolute top-4 left-4 text-[10px] uppercase tracking-wider bg-white/50 px-2 py-1 backdrop-blur-sm">{article.tag}</span>
                                    <!-- Use text overlay instead of image if image fails, but styling div with bg color -->
                                    <div class="text-center p-4">
                                        <!-- Placeholder graphic -->
                                        <div class="text-2xl font-serif italic opacity-50">{article.title.split(' ')[0]}</div>
                                    </div>
                                </div>
                                <h3 class="text-lg font-normal mb-3 leading-tight group-hover:underline decoration-1 underline-offset-4">
                                    {article.title}
                                </h3>
                                <p class="text-xs text-gray-500 mb-4 leading-relaxed">
                                    {article.desc}
                                </p>
                                <a href="#" class="text-xs font-medium underline decoration-1 underline-offset-4">Read more</a>
                            </div>
                        {/each}
                    </div>
                </section>

            </div>
        </div>
    </main>

    <!-- Footer -->
    <footer class="bg-white pt-32 pb-12 border-t border-gray-100 relative overflow-hidden">
        <!-- Large Background Watermark -->
        <div class="absolute left-0 bottom-0 text-[20vw] font-bold text-gray-50 leading-none select-none pointer-events-none -mb-12 -ml-12">
            CENTINEL
        </div>

        <div class="max-w-[1600px] mx-auto px-6 relative z-10">
            <div class="flex flex-col md:flex-row justify-between items-end md:items-center mb-24">
                <div class="text-lg font-light">Intelligence you can trust</div>
                <div class="text-lg font-light underline decoration-1 underline-offset-4">CENTINELANALYTICA.COM</div>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-12 gap-8 items-end">
                <div class="md:col-span-6">
                    <!-- Logo -->
                    <div class="flex items-center gap-4 mb-4">
                        <svg class="w-8 h-8 text-primary-600" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path
                                fill-rule="evenodd"
                                clip-rule="evenodd"
                                d="M6.99251 12.196C6.85314 12.5757 6.62925 12.9208 6.33682 13.2067H6.33835C6.00191 13.5351 5.58566 13.7756 5.12816 13.9059C4.67065 14.0362 4.18671 14.0522 3.72118 13.9523C3.25564 13.8524 2.82357 13.64 2.46501 13.3345C2.10645 13.0291 1.83299 12.6406 1.66998 12.2051C1.50697 11.7696 1.45969 11.3012 1.5325 10.8432C1.60532 10.3852 1.79587 9.95244 2.08653 9.58516C2.37718 9.21781 2.75852 8.9277 3.1952 8.74177C3.63188 8.55585 4.10979 8.48002 4.58462 8.52142L4.57074 8.50792C5.0567 8.54782 5.54575 8.48407 6.00378 8.32124C6.4618 8.15846 6.87776 7.90043 7.2226 7.56521C7.56746 7.22998 7.83285 6.82564 8.00036 6.38041C8.16786 5.93517 8.23344 5.45976 8.1924 4.98737L8.20628 5.00087C8.15181 4.43594 8.27796 3.86844 8.56753 3.37575C8.85701 2.88307 9.29579 2.48919 9.82407 2.24782C10.3523 2.00645 10.9443 1.92933 11.5192 2.02701C12.0942 2.12467 12.6243 2.39237 13.037 2.79358C13.4497 3.19479 13.7251 3.70999 13.8256 4.26892C13.926 4.82785 13.8467 5.4033 13.5984 5.9168C13.3501 6.4303 12.9449 6.85685 12.4381 7.13828C11.9313 7.41971 11.3474 7.54233 10.7663 7.4894L10.781 7.5029C10.2949 7.46279 9.80563 7.52632 9.34741 7.68904C8.88919 7.85176 8.47309 8.10975 8.12805 8.44499C7.78301 8.78025 7.51742 9.18466 7.34983 9.63001C7.18224 10.0754 7.11669 10.551 7.15774 11.0235L7.14309 11.01C7.1833 11.4112 7.13189 11.8162 6.99251 12.196ZM11.5077 14.7121L11.493 14.6986C11.9061 14.739 12.3232 14.6897 12.7143 14.5543C13.1053 14.4188 13.4605 14.2007 13.7542 13.9154C14.0477 13.6302 14.2726 13.285 14.4121 12.905C14.5518 12.525 14.6028 12.1196 14.5615 11.718L14.5762 11.7315C14.5351 11.2591 14.6007 10.7838 14.7681 10.3385C14.9356 9.89327 15.2011 9.48893 15.5459 9.15368C15.8908 8.8185 16.3068 8.56042 16.7648 8.39767C17.2228 8.23481 17.7118 8.17111 18.1978 8.21099L18.1832 8.19749C18.7645 8.25059 19.3485 8.12801 19.8556 7.84656C20.3627 7.56511 20.7681 7.13845 21.0165 6.62479C21.265 6.11114 21.3444 5.53548 21.2439 4.97634C21.1435 4.4172 20.868 3.9018 20.4551 3.50044C20.0422 3.09909 19.512 2.8313 18.9368 2.73364C18.3616 2.63596 17.7695 2.71315 17.241 2.95467C16.7126 3.19618 16.2737 3.59027 15.9842 4.08319C15.6946 4.57609 15.5685 5.14383 15.6232 5.70895L15.6093 5.6947C15.6504 6.16712 15.585 6.64259 15.4175 7.08788C15.2501 7.53318 14.9846 7.93758 14.6398 8.27287C14.2949 8.60805 13.8789 8.86612 13.4208 9.02888C12.9627 9.19163 12.4736 9.25523 11.9876 9.21526L12.0015 9.22951C11.5885 9.18908 11.1713 9.23836 10.7803 9.37381C10.3893 9.50919 10.034 9.72744 9.74039 10.0127C9.44674 10.2979 9.22199 10.6431 9.08234 11.0231C8.94276 11.4031 8.89176 11.8085 8.93304 12.2101L8.91915 12.1966C8.96005 12.6689 8.89439 13.1443 8.72688 13.5895C8.5593 14.0346 8.29389 14.4389 7.94908 14.7741C7.60425 15.1093 7.18835 15.3673 6.73039 15.5302C6.27242 15.693 5.78342 15.7569 5.29749 15.7171L5.31138 15.7306C4.73003 15.6775 4.14599 15.8001 3.63892 16.0815C3.13186 16.363 2.72644 16.7896 2.478 17.3033C2.22954 17.817 2.15013 18.3926 2.25061 18.9518C2.35109 19.5109 2.62657 20.0263 3.03945 20.4276C3.45234 20.829 3.98253 21.0968 4.55773 21.1944C5.13293 21.2921 5.72512 21.2149 6.25353 20.9734C6.78193 20.7319 7.22085 20.3379 7.51038 19.8449C7.79994 19.352 7.92601 18.7843 7.87139 18.2191L7.88605 18.2326C7.845 17.7602 7.91058 17.2849 8.07809 16.8396C8.24551 16.3944 8.511 15.99 8.85581 15.6548C9.20069 15.3196 9.61664 15.0615 10.0746 14.8988C10.5327 14.7359 11.0217 14.6722 11.5077 14.7121ZM17.1996 10.7633C16.9071 11.0493 16.6832 11.3944 16.5437 11.7741C16.4042 12.1538 16.3526 12.5587 16.3925 12.9601L16.3786 12.9466C16.4197 13.419 16.3541 13.8944 16.1866 14.3396C16.0191 14.7849 15.7537 15.1892 15.4089 15.5244C15.064 15.8596 14.648 16.1177 14.19 16.2804C13.732 16.4433 13.2429 16.507 12.757 16.4671L12.7708 16.4806C12.1896 16.4281 11.6057 16.551 11.0989 16.8328C10.5921 17.1145 10.1871 17.5414 9.93902 18.0551C9.69097 18.5689 9.61188 19.1444 9.71265 19.7035C9.81349 20.2625 10.0892 20.7777 10.5022 21.1788C10.9152 21.5799 11.4454 21.8474 12.0205 21.9448C12.5957 22.0423 13.1877 21.9649 13.716 21.7234C14.2443 21.4817 14.683 21.0877 14.9724 20.5947C15.2618 20.1018 15.3878 19.5342 15.3332 18.9692L15.3478 18.9827C15.3068 18.5103 15.3723 18.0349 15.5398 17.5896C15.7073 17.1444 15.9728 16.7401 16.3176 16.4048C16.6625 16.0696 17.0784 15.8115 17.5364 15.6488C17.9945 15.486 18.4835 15.4222 18.9695 15.4621L18.9548 15.4486C19.4296 15.4901 19.9076 15.4144 20.3444 15.2286C20.7811 15.0427 21.1625 14.7527 21.4533 14.3854C21.744 14.0181 21.9347 13.5854 22.0075 13.1274C22.0805 12.6694 22.0332 12.2009 21.8703 11.7653C21.7073 11.3298 21.4339 10.9413 21.0754 10.6358C20.7168 10.3303 20.2848 10.1178 19.8192 10.0179C19.3536 9.91795 18.8697 9.93385 18.4121 10.0641C17.9546 10.1945 17.5383 10.4349 17.2019 10.7633H17.1996Z"
                                fill="currentColor"
                            />
                        </svg>
                        <div class="text-sm font-medium leading-tight">
                            Centinel Analytica
                        </div>
                    </div>
                </div>
                
                <div class="md:col-span-6 flex flex-col md:flex-row justify-between items-end md:items-end gap-8">
                    <div class="text-[10px] text-gray-400">
                        © 2025 Centinel Analytica
                    </div>
                    
                    <div class="flex gap-8 text-[10px] font-medium uppercase tracking-wide">
                        <div class="flex flex-col gap-2">
                            <a href="#">Platform</a>
                            <a href="#">Intelligence</a>
                            <a href="#">Contact</a>
                        </div>
                        <div class="flex flex-col gap-2">
                            <a href="#">Terms</a>
                            <a href="#">Privacy Policy</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </footer>
</div>

<style>
    /* Custom scrollbar hide for clean look */
    ::-webkit-scrollbar {
        width: 0px;
        background: transparent;
    }
</style>

