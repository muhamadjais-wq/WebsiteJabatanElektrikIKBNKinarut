# WebsiteJabatanElektrikIKBNKinarut
<html lang="ms">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JABATAN ELEKTRIK IKBN KINARUT SABAH</title>
    <!-- Muat Naik Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Konfigurasi Tailwind untuk Font Inter dan Tema -->
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@100..900&display=swap');
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f7f7f7; /* Latar belakang cerah */
        }
        .text-ikbn-primary { color: #004d99; } /* Biru Korporat Gelap */
        .bg-ikbn-primary { background-color: #004d99; }
        .border-ikbn-primary { border-color: #004d99; }
        .text-ikbn-secondary { color: #ffcc00; } /* Emas/Kuning */
        .bg-ikbn-secondary { background-color: #ffcc00; }
        .shadow-ikbn { box-shadow: 0 10px 15px -3px rgba(0, 77, 153, 0.1), 0 4px 6px -2px rgba(0, 77, 153, 0.05); }
    </style>
    <!-- Ikon Lucide untuk profesionalisme -->
    <script type="module">
        import {
            Gauge, Zap, Target, Users, File, Phone, Link
        } from 'https://unpkg.com/lucide@latest';

        const icons = { Gauge, Zap, Target, Users, File, Phone, Link };

        document.querySelectorAll('[data-lucide]').forEach(el => {
            const iconName = el.getAttribute('data-lucide');
            if (icons[iconName]) {
                el.innerHTML = icons[iconName].toSvg({ class: el.className });
            }
        });
    </script>
</head>

<body class="antialiased text-gray-800">

    <!-- Navbar/Header -->
    <header class="bg-ikbn-primary shadow-ikbn sticky top-0 z-50">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex flex-col md:flex-row justify-between items-center">
            <h1 class="text-2xl font-extrabold text-white tracking-wider">JABATAN ELEKTRIK</h1>
            <h2 class="text-lg font-light text-ikbn-secondary mt-1 md:mt-0">IKBN KINARUT SABAH</h2>
            <nav class="hidden md:flex space-x-6">
                <a href="#misi-visi" class="text-white hover:text-ikbn-secondary transition duration-300 font-medium">Misi & Visi</a>
                <a href="#kursus" class="text-white hover:text-ikbn-secondary transition duration-300 font-medium">Kursus</a>
                <a href="#progression" class="text-white hover:text-ikbn-secondary transition duration-300 font-medium">Laluan Kerjaya</a>
                <a href="#hubungi" class="text-white hover:text-ikbn-secondary transition duration-300 font-medium">Hubungi</a>
            </nav>
        </div>
    </header>

    <main class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-10">

        <!-- Banner Hero Section -->
        <section class="mb-12 bg-white p-8 rounded-xl shadow-lg border-t-4 border-ikbn-secondary">
            <div class="flex items-center space-x-4">
                <div data-lucide="Zap" class="h-12 w-12 text-ikbn-primary flex-shrink-0"></div>
                <div>
                    <h2 class="text-3xl sm:text-4xl font-extrabold text-ikbn-primary">Program Kompetensi Elektrik</h2>
                    <p class="text-xl text-gray-600 mt-1">Lahirkan penjaga jentera bertauliah, kompeten, dan berdaya saing.</p>
                </div>
            </div>
            <!-- Peringatan Penting (MANDATORI) -->
            <div id="syarat-penting" class="mt-6 p-4 bg-red-100 text-red-800 border-l-4 border-red-500 rounded-md font-semibold">
                <div class="flex items-start">
                    <span data-lucide="File" class="h-5 w-5 mr-2 mt-0.5 flex-shrink-0"></span>
                    <p class="uppercase">
                        <strong class="text-red-900">PERINGATAN PENTING:</strong> Sila baca dan fahami
                        <a href="#syarat-am" class="underline hover:text-red-600">SYARAT KELAYAKAN LENGKAP</a> bagi setiap kursus sebelum membuat permohonan.
                    </p>
                </div>
            </div>
        </section>

        <!-- Misi & Visi Section -->
        <section id="misi-visi" class="grid md:grid-cols-2 gap-8 mb-12">
            <div class="bg-white p-6 rounded-xl shadow-lg border-l-4 border-ikbn-primary">
                <div class="flex items-center mb-3">
                    <span data-lucide="Target" class="h-6 w-6 text-ikbn-primary mr-2"></span>
                    <h3 class="text-2xl font-bold text-ikbn-primary">VISI</h3>
                </div>
                <p class="text-gray-600 leading-relaxed">
                    Menjadi institusi peneraju dalam melahirkan Penjaga Jentera Elektrik yang kompeten dan berdaya saing di peringkat kebangsaan dan antarabangsa.
                </p>
            </div>
            <div class="bg-white p-6 rounded-xl shadow-lg border-l-4 border-ikbn-primary">
                <div class="flex items-center mb-3">
                    <span data-lucide="Gauge" class="h-6 w-6 text-ikbn-primary mr-2"></span>
                    <h3 class="text-2xl font-bold text-ikbn-primary">MISI</h3>
                </div>
                <p class="text-gray-600 leading-relaxed">
                    Menyediakan program latihan elektrik bertaraf dunia yang diiktiraf ECoS, memastikan kecemerlangan akademik dan kemahiran praktikal, serta memupuk budaya keselamatan dan profesionalisme yang tinggi.
                </p>
            </div>
        </section>

        <!-- Kursus Separuh Masa Section (Tabbed Navigation) -->
        <section id="kursus" class="mb-12">
            <h2 class="text-3xl font-extrabold text-ikbn-primary mb-6 border-b-2 border-ikbn-secondary pb-2">INFO KURSUS SEPARUH MASA</h2>

            <!-- Tabs Navigation -->
            <div class="flex flex-wrap border-b border-gray-200" id="tab-nav-buttons">
                <button onclick="openTab(event, 'A0')" class="tab-button py-2 px-4 text-sm font-medium focus:outline-none transition-colors duration-300 border-b-2 border-transparent text-gray-600 hover:text-ikbn-primary hover:border-ikbn-primary active-tab bg-white">
                    Penjaga Jentera A0
                </button>
                <button onclick="openTab(event, 'A1')" class="tab-button py-2 px-4 text-sm font-medium focus:outline-none transition-colors duration-300 border-b-2 border-transparent text-gray-600 hover:text-ikbn-primary hover:border-ikbn-primary">
                    Penjaga Jentera A1
                </button>
                <button onclick="openTab(event, 'A4')" class="tab-button py-2 px-4 text-sm font-medium focus:outline-none transition-colors duration-300 border-b-2 border-transparent text-gray-600 hover:text-ikbn-primary hover:border-ikbn-primary">
                    Penjaga Jentera A4
                </button>
                <button onclick="openTab(event, 'B0')" class="tab-button py-2 px-4 text-sm font-medium focus:outline-none transition-colors duration-300 border-b-2 border-transparent text-gray-600 hover:text-ikbn-primary hover:border-ikbn-primary">
                    Penjaga Jentera B0 (11kV)
                </button>
            </div>

            <!-- Tabs Content -->
            <div id="tab-content" class="mt-6 bg-white p-6 rounded-xl shadow-lg">

                <!-- KURSUS A0 -->
                <div id="A0" class="tab-pane">
                    <h3 class="text-2xl font-bold text-ikbn-primary mb-4 flex items-center">
                        <span data-lucide="Zap" class="h-6 w-6 mr-2"></span>
                        PENJAGA JENTERA KATEGORI A0
                    </h3>
                    <p class="text-sm font-medium text-gray-500 mb-4">Tarikh Pentauliahan: 22 MAC 2024</p>
                    
                    <!-- Program IV -->
                    <div class="mb-6 p-4 border rounded-lg bg-gray-50">
                        <h4 class="text-xl font-semibold text-gray-700 mb-2">Program IV (480 Jam)</h4>
                        <ul class="list-disc ml-6 text-sm text-gray-600">
                            <li><strong>Sistem:</strong> Voltan Rendah Tanpa Talian Aerial & Stesen Janakuasa</li>
                            <li><strong>Tempoh:</strong> Separuh Masa (480 Jam, Tidak Kurang Dari 6 Bulan)</li>
                            <li><strong>Kapasiti:</strong> 30 Calon/Sesi (2 Sesi Setahun)</li>
                        </ul>
                        <div class="mt-4">
                            <h5 class="text-base font-bold text-red-700">SYARAT KELAYAKAN SEPARUH MASA (PROGRAM IV)</h5>
                            <ol class="list-decimal ml-6 text-sm space-y-1 mt-1 text-gray-700">
                                <li>Warganegara Malaysia.</li>
                                <li>Berumur tidak kurang dari 20 tahun semasa menduduki peperiksaan.</li>
                                <li>Boleh bertutur dan menulis dalam Bahasa Kebangsaan.</li>
                                <li>Memiliki kelayakan Pendidikan, sekurang-kurangnya tamat tingkatan lima (5) sekolah bantuan penuh Kerajaan.</li>
                                <li>Kehadiran mestilah tidak kurang dari 90% (Pembelajaran di institusi adalah 60% teori dan 40% amali).</li>
                                <li>Bekerja tidak kurang daripada tiga (3) tahun dalam persekitaran pengendalian kelengkapan elektrik dan pengalaman mengawal kelengkapan hidup.</li>
                                <li>Memiliki buku log lengkap berkaitan pengalaman kerja di atas, disahkan oleh orang kompeten dan majikan.</li>
                                <li><strong class="text-ikbn-primary">ATAU:</strong> Mempunyai perakuan kekompetenan Pendawai PW1/PW2 atau PW3/PW4 atau PW6 atau Sijil Politeknik (Kejuruteraan Elektrik).</li>
                                <li><strong class="text-ikbn-primary">DAN:</strong> Berpengalaman kerja tidak kurang daripada dua (2) tahun dalam persekitaran pengendalian kelengkapan elektrik dan pengalaman mengawal kelengkapan hidup.</li>
                            </ol>
                        </div>
                    </div>

                    <!-- Program V (Modul) -->
                    <div class="p-4 border rounded-lg bg-gray-50">
                        <h4 class="text-xl font-semibold text-gray-700 mb-2">Program V - MODUL (80 Jam)</h4>
                        <ul class="list-disc ml-6 text-sm text-gray-600">
                            <li><strong>Modul:</strong> Papan Suis Utama & Kawalan Motor Voltan Rendah</li>
                            <li><strong>Tempoh:</strong> Separuh Masa (80 Jam - 10 Hari)</li>
                            <li><strong>Kapasiti:</strong> 30 Calon/Sesi (2 Sesi Setahun)</li>
                        </ul>
                        <div class="mt-4">
                            <h5 class="text-base font-bold text-red-700">SYARAT KELAYAKAN SEPARUH MASA (PROGRAM V)</h5>
                            <ol class="list-decimal ml-6 text-sm space-y-1 mt-1 text-gray-700">
                                <li>Memenuhi syarat am (Warganegara, umur min 20 tahun, Bahasa Kebangsaan, tamat Tingkatan 5).</li>
                                <li>Mengemukakan surat layak mengikuti kursus modul daripada ECoS.</li>
                                <li>Menyertakan penyata KWSP atau SOCSO sebagai bukti bekerja dengan majikan yang mengesahkan keperluan Penjaga Jentera Terhad.</li>
                            </ol>
                            <p class="text-sm font-semibold mt-2">PENGALAMAN MANDATORI:</p>
                            <ul class="list-disc ml-6 text-xs text-gray-600">
                                <li>Tidak kurang daripada tiga (3) tahun dalam persekitaran pengendalian kelengkapan elektrik dan pengalaman mengawal kelengkapan hidup.</li>
                                <li>Tidak kurang enam (6) bulan di pepasangan tempat pemohon bekerja.</li>
                                <li>Pemohon dikehendaki mengemukakan buku log kerja harian.</li>
                            </ul>
                            <p class="text-xs italic mt-2 text-ikbn-primary">Nota: Sijil Modul ini melayakkan pemegangnya untuk memohon perakuan kekompetenan Penjaga Jentera A0 Terhad.</p>
                        </div>
                    </div>
                    <div class="flex justify-end mt-4">
                        <a href="https://forms.gle/ZeXBrrAGaYtxr2u67" target="_blank" class="bg-ikbn-secondary text-ikbn-primary font-bold py-2 px-6 rounded-lg hover:bg-yellow-600 transition duration-300 flex items-center shadow-md">
                             <span data-lucide="Link" class="h-4 w-4 mr-2"></span> Borang Permohonan A0
                        </a>
                    </div>
                </div>

                <!-- KURSUS A1 -->
                <div id="A1" class="tab-pane hidden">
                    <h3 class="text-2xl font-bold text-ikbn-primary mb-4 flex items-center">
                        <span data-lucide="Zap" class="h-6 w-6 mr-2"></span>
                        PENJAGA JENTERA KATEGORI A1
                    </h3>
                    <p class="text-sm font-medium text-gray-500 mb-4">No. Sijil Pentauliahan: ECOS/JKP/IL(E)/027-2024</p>
                    
                    <!-- Program III -->
                    <div class="mb-6 p-4 border rounded-lg bg-gray-50">
                        <h4 class="text-xl font-semibold text-gray-700 mb-2">Program III (540 Jam)</h4>
                        <ul class="list-disc ml-6 text-sm text-gray-600">
                            <li><strong>Sistem:</strong> Voltan Rendah Tanpa Stesen Janakuasa</li>
                            <li><strong>Tempoh:</strong> Separuh Masa (540 Jam, Tidak Kurang Dari 6 Bulan)</li>
                            <li><strong>Kapasiti:</strong> 30 Calon/Sesi (2 Sesi Setahun)</li>
                        </ul>
                        <div class="mt-4">
                            <h5 class="text-base font-bold text-red-700">SYARAT KELAYAKAN SEPARUH MASA (PROGRAM III)</h5>
                            <ol class="list-decimal ml-6 text-sm space-y-1 mt-1 text-gray-700">
                                <li>Memenuhi syarat am Program I (Warganegara, umur min 20 tahun, Bahasa Kebangsaan, tamat Tingkatan 5).</li>
                                <li>Kehadiran mestilah tidak kurang dari 90% (60% teori dan 40% amali).</li>
                                <li>Bekerja tidak kurang daripada tiga (3) tahun dalam persekitaran pengendalian kelengkapan elektrik dan pengalaman mengawal kelengkapan hidup.</li>
                                <li>Memiliki buku log lengkap (2 tahun pengendalian, 1 tahun pemasangan/penyelenggaraan talian atas VR).</li>
                                <li><strong class="text-ikbn-primary">ATAU:</strong> Perakuan Kekompetenan Penjaga Jentera A0 + 1 tahun pengalaman dalam pemasangan/penyelenggaraan talian atas VR.</li>
                                <li><strong class="text-ikbn-primary">ATAU:</strong> Perakuan Kekompetenan Pendawai + 2 tahun pengalaman kerja (1 tahun pengendalian, 1 tahun pemasangan/penyelenggaraan talian atas VR).</li>
                            </ol>
                        </div>
                    </div>

                    <!-- Program IV (Modul TAVR) -->
                    <div class="p-4 border rounded-lg bg-gray-50">
                        <h4 class="text-xl font-semibold text-gray-700 mb-2">Program IV - MODUL (80 Jam)</h4>
                        <ul class="list-disc ml-6 text-sm text-gray-600">
                            <li><strong>Modul:</strong> Talian Atas Voltan Rendah (TAVR)</li>
                            <li><strong>Tempoh:</strong> Sepenuh/Separuh Masa (80 Jam)</li>
                            <li><strong>Kapasiti:</strong> 30 Calon/Sesi (2 Sesi Setahun)</li>
                        </ul>
                        <div class="mt-4">
                            <h5 class="text-base font-bold text-red-700">SYARAT KELAYAKAN MODUL TAVR</h5>
                            <ol class="list-decimal ml-6 text-sm space-y-1 mt-1 text-gray-700">
                                <li>Memenuhi syarat am (Warganegara, umur min 20 tahun, Bahasa Kebangsaan, tamat Tingkatan 5).</li>
                                <li>Memiliki perakuan kekompetenan A0 tidak kurang satu (1) tahun.</li>
                                <li>Memiliki buku log yang lengkap berkaitan kerja-kerja dan pengalaman di atas yang telah disahkan.</li>
                            </ol>
                            <p class="text-xs italic mt-2 text-ikbn-primary">Nota: Sijil Modul TAVR ini boleh digunakan untuk menggantikan pengalaman kerja talian atas VR bagi calon A1.</p>
                        </div>
                    </div>
                    <div class="flex justify-end mt-4 space-x-2">
                        <a href="https://forms.gle/wtq2pc6yYB7UjzM59" target="_blank" class="bg-ikbn-primary text-white font-bold py-2 px-6 rounded-lg hover:bg-ikbn-primary/90 transition duration-300 flex items-center shadow-md">
                             <span data-lucide="Link" class="h-4 w-4 mr-2"></span> Borang Modul TAVR
                        </a>
                        <a href="https://forms.gle/TJpNuYjMt9GUGNHG8" target="_blank" class="bg-ikbn-secondary text-ikbn-primary font-bold py-2 px-6 rounded-lg hover:bg-yellow-600 transition duration-300 flex items-center shadow-md">
                             <span data-lucide="Link" class="h-4 w-4 mr-2"></span> Borang Permohonan A1
                        </a>
                    </div>
                </div>

                <!-- KURSUS A4 -->
                <div id="A4" class="tab-pane hidden">
                    <h3 class="text-2xl font-bold text-ikbn-primary mb-4 flex items-center">
                        <span data-lucide="Zap" class="h-6 w-6 mr-2"></span>
                        PENJAGA JENTERA KATEGORI A4
                    </h3>
                    <p class="text-sm font-medium text-gray-500 mb-4">No. Sijil Pentauliahan: ECOS/JKP/IL(E)/029-2024</p>
                    
                    <!-- Program III -->
                    <div class="mb-6 p-4 border rounded-lg bg-gray-50">
                        <h4 class="text-xl font-semibold text-gray-700 mb-2">Program III (600 Jam)</h4>
                        <ul class="list-disc ml-6 text-sm text-gray-600">
                            <li><strong>Sistem:</strong> Sistem Voltan Rendah dengan Janakuasa Segerak</li>
                            <li><strong>Tempoh:</strong> Separuh Masa (600 Jam, Tidak Kurang Dari 10 Bulan)</li>
                            <li><strong>Kapasiti:</strong> 30 Calon/Sesi (2 Sesi Setahun)</li>
                        </ul>
                        <div class="mt-4">
                            <h5 class="text-base font-bold text-red-700">SYARAT KELAYAKAN SEPARUH MASA (PROGRAM III)</h5>
                            <ol class="list-decimal ml-6 text-sm space-y-1 mt-1 text-gray-700">
                                <li>Memenuhi syarat am (Warganegara, umur min 20 tahun, Bahasa Kebangsaan, tamat Tingkatan 5).</li>
                                <li><strong class="text-ikbn-primary">Pilihan 1:</strong> Perakuan Kekompetenan Penjaga Jentera A0 + 1 tahun pengalaman janakuasa segerak VR + 1 tahun pengalaman pemasangan/penyelenggaraan talian atas VR.</li>
                                <li><strong class="text-ikbn-primary">Pilihan 2:</strong> Perakuan Kekompetenan Penjaga Jentera A1 + 1 tahun pengalaman janakuasa segerak VR.</li>
                                <li><strong class="text-ikbn-primary">Pilihan 3:</strong> Perakuan Kekompetenan Penjaga Jentera A4-1 + 1 tahun pengalaman janakuasa segerak VR.</li>
                                <li>Wajib memiliki buku log lengkap bagi tempoh pengalaman berkenaan.</li>
                            </ol>
                        </div>
                    </div>

                    <!-- Program IV (Modul JKVR) -->
                    <div class="p-4 border rounded-lg bg-gray-50">
                        <h4 class="text-xl font-semibold text-gray-700 mb-2">Program IV - MODUL (80 Jam)</h4>
                        <ul class="list-disc ml-6 text-sm text-gray-600">
                            <li><strong>Modul:</strong> Janakuasa Voltan Rendah Dengan Penyegerakan (JKVR)</li>
                            <li><strong>Tempoh:</strong> Sepenuh/Separuh Masa (80 Jam)</li>
                            <li><strong>Kapasiti:</strong> 30 Calon/Sesi (2 Sesi Setahun)</li>
                        </ul>
                        <div class="mt-4">
                            <h5 class="text-base font-bold text-red-700">SYARAT KELAYAKAN MODUL JKVR</h5>
                            <ol class="list-decimal ml-6 text-sm space-y-1 mt-1 text-gray-700">
                                <li>Memenuhi syarat am (Warganegara, umur min 20 tahun, Bahasa Kebangsaan, tamat Tingkatan 5).</li>
                                <li>Memiliki perakuan kekompetenan A0 tidak kurang dua (2) tahun.</li>
                                <li><strong class="text-ikbn-primary">ATAU:</strong> Memiliki perakuan kekompetenan A1 tidak kurang satu (1) tahun.</li>
                                <li>Memiliki buku log yang lengkap berkaitan kerja-kerja dan pengalaman di atas yang telah disahkan.</li>
                            </ol>
                            <p class="text-xs italic mt-2 text-ikbn-primary">Nota: Modul ini adalah sebagai ganti pengalaman satu (1) tahun janakuasa segerak VR.</p>
                        </div>
                    </div>
                    <div class="flex justify-end mt-4 space-x-2">
                        <a href="https://forms.gle/acb7zLHTXScLzYoJ7" target="_blank" class="bg-ikbn-primary text-white font-bold py-2 px-6 rounded-lg hover:bg-ikbn-primary/90 transition duration-300 flex items-center shadow-md">
                             <span data-lucide="Link" class="h-4 w-4 mr-2"></span> Borang Modul JKVR
                        </a>
                        <a href="https://forms.gle/28Fy1RD8dZukcUrP6" target="_blank" class="bg-ikbn-secondary text-ikbn-primary font-bold py-2 px-6 rounded-lg hover:bg-yellow-600 transition duration-300 flex items-center shadow-md">
                             <span data-lucide="Link" class="h-4 w-4 mr-2"></span> Borang Permohonan A4
                        </a>
                    </div>
                </div>

                <!-- KURSUS B0 -->
                <div id="B0" class="tab-pane hidden">
                    <h3 class="text-2xl font-bold text-ikbn-primary mb-4 flex items-center">
                        <span data-lucide="Zap" class="h-6 w-6 mr-2"></span>
                        PENJAGA JENTERA KATEGORI B0 (11kV)
                    </h3>
                    <p class="text-sm font-medium text-gray-500 mb-4">No. Sijil Pentauliahan: ECOS/JKP/IL(E)/030-2024</p>
                    
                    <!-- Program II -->
                    <div class="mb-6 p-4 border rounded-lg bg-gray-50">
                        <h4 class="text-xl font-semibold text-gray-700 mb-2">Program II (600 Jam)</h4>
                        <ul class="list-disc ml-6 text-sm text-gray-600">
                            <li><strong>Sistem:</strong> Voltan Tinggi (11kV)</li>
                            <li><strong>Tempoh:</strong> Separuh Masa (600 Jam, Tidak Kurang Dari 10 Bulan)</li>
                            <li><strong>Kapasiti:</strong> 30 Calon/Sesi (2 Sesi Setahun)</li>
                        </ul>
                        <div class="mt-4">
                            <h5 class="text-base font-bold text-red-700">SYARAT KELAYAKAN SEPARUH MASA (PROGRAM II)</h5>
                            <ol class="list-decimal ml-6 text-sm space-y-1 mt-1 text-gray-700">
                                <li>Memenuhi syarat am Program I (Warganegara, umur min 20 tahun, Bahasa Kebangsaan, tamat Tingkatan 5).</li>
                                <li>Kehadiran mestilah tidak kurang dari 95% (60% teori dan 40% amali).</li>
                                <li><strong class="text-ikbn-primary">Pilihan 1:</strong> Perakuan Kekompetenan Penjaga Jentera A4 + 2 tahun pengalaman dalam sistem voltan tinggi.</li>
                                <li><strong class="text-ikbn-primary">Pilihan 2:</strong> Perakuan Kekompetenan Penjaga Jentera B0-1 + 1 tahun janakuasa segerak VR.</li>
                                <li>Wajib memiliki buku log lengkap bagi tempoh pengalaman berkenaan.</li>
                            </ol>
                        </div>
                    </div>

                    <!-- Modul Kendalian Pencawang -->
                    <div class="p-4 border rounded-lg bg-gray-50">
                        <h4 class="text-xl font-semibold text-gray-700 mb-2">MODUL Kendalian Pencawang 11kV (80 Jam)</h4>
                        <ul class="list-disc ml-6 text-sm text-gray-600">
                            <li><strong>Tempoh:</strong> Separuh Masa (80 Jam)</li>
                            <li><strong>Kapasiti:</strong> 20 Calon/Sesi (2 Sesi Setahun)</li>
                        </ul>
                        <div class="mt-4">
                            <h5 class="text-base font-bold text-red-700">SYARAT KELAYAKAN MODUL KENDALIAN PENCAWANG</h5>
                            <ol class="list-decimal ml-6 text-sm space-y-1 mt-1 text-gray-700">
                                <li>Memenuhi syarat am (Warganegara, umur min 20 tahun, Bahasa Kebangsaan, tamat Tingkatan 5).</li>
                                <li>Memiliki perakuan kekompetenan Penjaga Jentera Kategori voltan rendah dan telah berdaftar dengan ECoS di pepasangan.</li>
                                <li>Surat pengesahan majikan mengenai keperluan pemohon sebagai Penjaga Jentera Terhad di pepasangannya.</li>
                                <li>Pengalaman tidak kurang tiga (3) tahun dalam persekitaran pengendalian kelengkapan elektrik dan pengalaman mengawal kelengkapan hidup.</li>
                            </ol>
                            <p class="text-xs italic mt-2 text-ikbn-primary">Nota: Sijil Modul ini melayakkan pemegangnya untuk memohon perakuan kekompetenan Penjaga Jentera A0 Terhad.</p>
                        </div>
                    </div>
                    <div class="flex justify-end mt-4 space-x-2">
                         <!-- LINK BARU DITAMBAH -->
                        <a href="https://forms.gle/3cAfRxsn9AQe63Mv5" target="_blank" class="bg-ikbn-primary text-white font-bold py-2 px-6 rounded-lg hover:bg-ikbn-primary/90 transition duration-300 flex items-center shadow-md">
                             <span data-lucide="Link" class="h-4 w-4 mr-2"></span> Borang Modul Pencawang 11kV
                        </a>
                        <a href="https://forms.gle/zaMeYgkWMUbQ1HP18" target="_blank" class="bg-ikbn-secondary text-ikbn-primary font-bold py-2 px-6 rounded-lg hover:bg-yellow-600 transition duration-300 flex items-center shadow-md">
                             <span data-lucide="Link" class="h-4 w-4 mr-2"></span> Borang Permohonan B0
                        </a>
                    </div>
                </div>
            </div>
        </section>

        <!-- Syarat Kelayakan Am Mandatori -->
        <section id="syarat-am" class="mb-12 p-8 bg-ikbn-primary text-white rounded-xl shadow-lg">
            <h2 class="text-3xl font-extrabold text-ikbn-secondary mb-4 flex items-center">
                <span data-lucide="Users" class="h-6 w-6 mr-2"></span>
                SYARAT KELAYAKAN AM MANDATORI
            </h2>
            <p class="mb-4 font-light">Semua pemohon bagi kursus-kursus kompetensi elektrik di IKBN Kinarut adalah **WAJIB** memenuhi syarat-syarat berikut:</p>
            <ol class="list-decimal ml-6 space-y-2 font-medium">
                <li><strong class="text-ikbn-secondary">MEMILIKI NOMBOR KOMPETEN ATAU KOMPETEN ECOS SABAH</strong></li>
                <li><strong class="text-ikbn-secondary">BEKERJA DENGAN SYARIKAT ELEKTRIK YANG BERDAFTAR DENGAN ECOS SABAH</strong></li>
                <li><strong class="text-ikbn-secondary">MEMPUNYAI SEKURANG-KURANGNYA TAMAT TINGKATAN LIMA (5)</strong></li>
            </ol>
            <p class="mt-4 text-sm italic">Sila pastikan dokumen sokongan (surat sokongan, penyata KWSP/SOCSO, dll.) disediakan sebelum permohonan.</p>
        </section>

        <!-- Laluan Kemajuan Kompetensi (Progression Chart) -->
        <section id="progression" class="mb-12 p-8 bg-white rounded-xl shadow-lg">
            <h2 class="text-3xl font-extrabold text-ikbn-primary mb-6 border-b-2 border-ikbn-secondary pb-2">LALUAN KEMAJUAN KOMPETENSI (CARTA ALIR)</h2>
            <p class="text-gray-600 mb-6">Carta alir ini menunjukkan perjalanan standard kemajuan kompetensi Penjaga Jentera Elektrik:</p>

            <div class="flex flex-col items-center space-y-6 text-center">

                <!-- Laluan A0 -->
                <div class="w-full bg-ikbn-secondary/20 p-4 rounded-lg">
                    <p class="font-bold text-ikbn-primary text-lg mb-2">Laluan Bermula dari A0</p>
                    <div class="flex flex-wrap justify-center items-center gap-2 sm:gap-4">
                        <div class="flow-step bg-ikbn-primary text-white p-3 rounded-lg shadow-md font-semibold text-sm sm:text-base">
                            A0 (1 TAHUN BERDAFTAR ECOS)
                        </div>
                        <span class="text-ikbn-primary font-bold hidden sm:block">&rarr;</span>
                        <div class="flow-step bg-gray-200 text-gray-700 p-3 rounded-lg shadow-md font-semibold text-sm sm:text-base">
                            TAVR (80 JAM MODUL)
                        </div>
                        <span class="text-ikbn-primary font-bold hidden sm:block">&rarr;</span>
                        <div class="flow-step bg-gray-200 text-gray-700 p-3 rounded-lg shadow-md font-semibold text-sm sm:text-base">
                            JKVR (80 JAM MODUL)
                        </div>
                        <span class="text-ikbn-primary font-bold hidden sm:block">&rarr;</span>
                        <div class="flow-step bg-ikbn-secondary text-ikbn-primary p-3 rounded-lg shadow-md font-semibold text-sm sm:text-base">
                            A4
                        </div>
                        <span class="text-ikbn-primary font-bold hidden sm:block">&rarr;</span>
                        <div class="flow-step bg-ikbn-primary text-white p-3 rounded-lg shadow-md font-semibold text-sm sm:text-base">
                            B0 (11kV)
                        </div>
                    </div>
                </div>

                <!-- Laluan A1 -->
                <div class="w-full bg-ikbn-secondary/20 p-4 rounded-lg">
                    <p class="font-bold text-ikbn-primary text-lg mb-2">Laluan Bermula dari A1</p>
                    <div class="flex flex-wrap justify-center items-center gap-2 sm:gap-4">
                        <div class="flow-step bg-ikbn-primary text-white p-3 rounded-lg shadow-md font-semibold text-sm sm:text-base">
                            A1 (1 TAHUN BERDAFTAR ECOS)
                        </div>
                        <span class="text-ikbn-primary font-bold hidden sm:block">&rarr;</span>
                        <div class="flow-step bg-gray-200 text-gray-700 p-3 rounded-lg shadow-md font-semibold text-sm sm:text-base">
                            JKVR (80 JAM MODUL)
                        </div>
                        <span class="text-ikbn-primary font-bold hidden sm:block">&rarr;</span>
                        <div class="flow-step bg-ikbn-secondary text-ikbn-primary p-3 rounded-lg shadow-md font-semibold text-sm sm:text-base">
                            A4
                        </div>
                        <span class="text-ikbn-primary font-bold hidden sm:block">&rarr;</span>
                        <div class="flow-step bg-ikbn-primary text-white p-3 rounded-lg shadow-md font-semibold text-sm sm:text-base">
                            B0 (11kV)
                        </div>
                    </div>
                </div>

                <a href="https://drive.google.com/file/d/1QNYKrktL-sX9zWkVCY_go1hN75sSM462/view" target="_blank" class="mt-6 bg-red-600 text-white font-bold py-3 px-8 rounded-lg hover:bg-red-700 transition duration-300 flex items-center shadow-lg">
                    <span data-lucide="File" class="h-5 w-5 mr-2"></span> Muat Turun Borang Permohonan Kursus ECOS
                </a>
            </div>
        </section>

    </main>

    <!-- Footer & Contact -->
    <footer id="hubungi" class="bg-ikbn-primary py-8 mt-12">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
            <h3 class="text-2xl font-bold text-ikbn-secondary mb-4">HUBUNGI KAMI</h3>
            <div class="flex flex-col items-center text-white space-y-3">
                <div class="flex items-center space-x-2">
                    <span data-lucide="Phone" class="h-5 w-5 text-ikbn-secondary"></span>
                    <span class="font-semibold">EN. MUHAMAD JAIS BIN JALUN</span>
                </div>
                <div class="text-lg font-extrabold">
                    017-898 6747
                </div>
                <p class="text-sm italic text-ikbn-secondary bg-ikbn-primary p-2 rounded-md border border-ikbn-secondary">
                    *Hanya pada waktu bekerja sahaja.
                </p>
                <p class="text-sm mt-4 text-gray-300">&copy; 2024 Jabatan Elektrik IKBN Kinarut Sabah. Hak Cipta Terpelihara.</p>
            </div>
        </div>
    </footer>

    <script>
        // Fungsi untuk menguruskan tab kursus
        function openTab(evt, tabName) {
            var i, tabcontent, tablinks;
            
            // Sembunyikan semua tab content
            tabcontent = document.getElementsByClassName("tab-pane");
            for (i = 0; i < tabcontent.length; i++) {
                tabcontent[i].style.display = "none";
            }
            
            // Buang kelas 'active' dari semua butang
            tablinks = document.getElementsByClassName("tab-button");
            for (i = 0; i < tablinks.length; i++) {
                tablinks[i].classList.remove("text-ikbn-primary", "border-ikbn-primary", "active-tab", "bg-white", "font-bold");
                tablinks[i].classList.add("text-gray-600", "border-transparent", "font-medium");
            }
            
            // Tunjukkan tab content yang dipilih dan tandakan butang sebagai aktif
            document.getElementById(tabName).style.display = "block";
            evt.currentTarget.classList.remove("text-gray-600", "border-transparent", "font-medium");
            evt.currentTarget.classList.add("text-ikbn-primary", "border-ikbn-primary", "active-tab", "bg-white", "font-bold");
        }

        // Tetapkan tab pertama (A0) sebagai lalai apabila halaman dimuat
        window.onload = function() {
            // Dapatkan butang tab pertama dan klikkannya secara programatik
            const firstTabButton = document.querySelector('#tab-nav-buttons .tab-button');
            if (firstTabButton) {
                // Panggil openTab dengan event simulasi dan nama tab yang betul (A0)
                openTab({ currentTarget: firstTabButton }, 'A0');
            }
        };

    </script>
</body>
</html>
