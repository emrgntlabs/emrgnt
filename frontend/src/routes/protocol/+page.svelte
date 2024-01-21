<script>
    import Editor from '@tinymce/tinymce-svelte';

    let tinymceApiKey = import.meta.env.VITE_TINY_MCE_API_KEY;

    let showGenerateProtocolDialog = false;
    let protocol = "";
    let generateProtocolPrompt = "";

    const resetGenerateProtocol = () => {
        showGenerateProtocolDialog = false;
    }

    const generateProtocol = () => {
        protocol = 
        `
        <h1>Lab Protocol for Preparing Acute Horizontal VTA Brain Slices from Mice</h1>        
        <h2>Introduction</h2>
        This protocol outlines the preparation of acute horizontal brain slices from the ventral tegmental
        area (VTA) of mice for electrophysiological recordings. The use of N-Methyl-D-glucamine
        (NMDG) in the cutting solution is critical to prevent excitotoxicity during the slicing process.

        <h2>Materials and Reagents</h2>
        <ul>
            <li>Adult mice (C57BL/6 strain recommended)</li>
            <li>Isoflurane (Sigma-Aldrich, Catalog #I653)</li>
<li>        NMDG (Sigma-Aldrich, Catalog #M2004)</li>
<li>        HEPES (Sigma-Aldrich, Catalog #H3375)</li>
<li>        Glucose (Sigma-Aldrich, Catalog #G8270)</li>
<li>        NaHCO3 (Sigma-Aldrich, Catalog #S5761)</li>
<li>        NaH2PO4 (Sigma-Aldrich, Catalog #S3139)</li>
<li>        KCl (Sigma-Aldrich, Catalog #P9333)</li>
<li>        Sodium ascorbate (Sigma-Aldrich, Catalog #A4034)</li>
<li>        Sodium pyruvate (Sigma-Aldrich, Catalog #P5280)</li>
<li>        Thiourea (Sigma-Aldrich, Catalog #T8656)</li>
<li>        MgSO4 (Sigma-Aldrich, Catalog #M7506)</li>
<li>        CaCl2 (Sigma-Aldrich, Catalog #C5670)</li>
<li>        Sucrose (Sigma-Aldrich, Catalog #S0389)</li>
<li>        Agarose, low gelling point (Sigma-Aldrich, Catalog #A9414)</li>
<li>        Carbogen gas (95% O2/5% CO2)</li>
<li>        Artificial cerebrospinal fluid (ACSF)</li>
<li>        Vibratome (Leica VT1200s or equivalent)</li>
<li>        Dissection tools (scissors, forceps, spatulas)</li>
<li>        Ice and ice bucket</li>
<li>        Beakers and graduated cylinders</li>
<li>        Magnetic stirrer and stir bars</li>
<li>        pH meter</li>
<li>        Osmometer</li>
<li>        Water bath</li>
<li>        Suction device</li>
<li>        Recording chamber for electrophysiology</li>
<li>        Microscope with appropriate lighting</li>
        </ul>
        

        <h2>Solutions Preparation</h2>
        <h3>NMDG Cutting Solution (500 mL)</h3>
        <ul>
            <li>        110 mM NMDG: 9.53 g</li>
<li>        20 mM HEPES: 2.38 g</li>
<li>        25 mM Glucose: 2.25 g</li>
<li>        30 mM NaHCO3: 2.10 g</li>
<li>        1.2 mM NaH2PO4: 0.072 g</li>
<li>        2.5 mM</li>
<li>        KCl: 0.093 g</li>
<li>        5 mM Sodium ascorbate: 0.495 g</li>
<li>        3 mM Sodium pyru</li>
<li>        vate: 0.165 g</li>
<li>        2 mM Thiourea: 0.152 g</li>
<li>        10 mM MgSO4: 1.20 g</li>
<li>        0.5 mM CaCl2: 0.037 g</li>
<li>        Adjust pH to 7.4 with HCl</li>
<li>        1/20/24, 7:00 PM Emergnt</li>
<li>        Osmolarity: 305-310 mOsm</li>
<li>        Continuously bubble with carbogen gas</li>
        </ul>
        
        <h3>ACSF (500 mL)</h3>
        <ul>
            <li>        119 mM NaCl: 3.48 g</li>
<li>        26 mM NaHCO3: 1.09 g</li>
<li>        1 mM NaH2PO4: 0.060 g</li>
<li>        2.5 mM</li>
<li>        KCl: 0.093 g</li>
<li>        11 mM Glucose: 0.99 g</li>
<li>        10 mM Sucrose: 1.71 g</li>
<li>        2.5 mM MgSO4: 0.300 g</li>
<li>        2.5 mM CaCl2: 0.092 g</li>
<li>        Adjust pH to 7.4 with HCl</li>
<li>        Osmolarity: 295-305 mOsm</li>
<li>        Continuously bubble with carbogen gas</li>
        </ul>
        
        <h2>Equipment and Workspace Preparation</h2>
        <ol>
            <li>Clean and sterilize all dissection tools and vibratome.</li>
<li>Set up the vibratome according to the manufacturer's instructions.</li>
<li>Pre-chill the vibratome buffer tray with ice or a cooling block.</li>
<li>Prepare a water bath set to 32-34°C for slice recovery.</li>
<li>Arrange the dissection area with a cold block or ice pack to keep the brain cool during extraction.</li>
<li>Set up the recording chamber and ensure that the perfusion system is working correctly.</li>
<li>Calibrate the pH meter and osmometer.</li>
        </ol>

        <h2>Animal Anesthesia and Brain Extraction</h2>
        <ol>
            <li>Anesthetize the mouse with isoflurane until it is unresponsive to toe pinch.</li>
<li>Decapitate the mouse with surgical scissors and quickly remove the brain using dissection tools, being careful to avoid damaging the VTA.</li>
<li>Place the brain in ice-cold NMDG cutting solution immediately to prevent excitotoxicity.</li>
        </ol>


        <h2>Brain Sectioning</h2>
        <ol>
            <li>Trim the brain to isolate the region containing the VTA.</li>
<li>Embed the trimmed brain in low-gelling-point agarose prepared in NMDG cutting solution.</li>
<li>Mount the agarose block onto the vibratome stage and submerge it in ice-cold NMDG cutting solution.</li>
<li>Cut horizontal slices of the VTA at 200-300 μm thickness using the vibratome.</li>
<li>Collect slices and allow them to recover in a 32-34°C ACSF bath for 12 minutes, then at room temperature for at least 45 minutes before transferring to the recording chamber.</li>
        </ol>

        
        <h2>Tips for Success</h2>
        <ul>
            <li>Ensure that all solutions are freshly prepared and continuously bubbled with carbogen gas to maintain pH and oxygenation.</li>
<li>Keep the brain and slices cool at all times until the recovery step to minimize metabolic activity and potential damage.</li>
<li>Use a sharp vibratome blade to ensure clean cuts and reduce mechanical trauma to the tissue.</li>
<li>Handle brain tissue and slices gently with a paintbrush or similar soft tool to avoid physical damage.</li>
<li>Monitor the osmolarity of all solutions to ensure they are within the physiological range.</li>
        </ul>

        <h2>Conclusion</h2>
        Following this protocol should yield healthy, viable horizontal VTA brain slices suitable for electrophysiological recordings. It is crucial to maintain a sterile environment, handle the brain tissue gently, and ensure that all solutions are correctly prepared and maintained to achieve the best results

        <h2>Sources</h2>
        <ul>
            <li>Source Document: Bio-protocol4061.pdf | Page: 5.0</li>
<li>Source Document: 2363.pdf | Page: 11.0</li>
<li>Source Document: Bio-protocol2090.pdf | Page: 13.0</li>
<li>Source Document: Bio-protocol3890.pdf | Page: 7.0</li>
<li>Source Document: cell_pdf_S0092-8674(22)00146-5.pdf | Page: 22.0</li>
        </ul>
        `;

        resetGenerateProtocol();
    }

    let tinymceConf = {
        height:"calc(100vh - 32px)",
        skin:"borderless",
        toolbar: "undo redo | styleselect | bold italic | alignleft aligncenter alignright alignjustify | outdent | assistant",
        setup: function(editor) {
            editor.ui.registry.addMenuButton('assistant', {
                icon: "ai-prompt",
                fetch: (callback, fetchContext) => {
                    const items = [
                        {
                        type: 'menuitem',
                        text: 'Generate Lab Protocol',
                        
                        onAction: () => showGenerateProtocolDialog = true
                        },
                    ];
                    callback(items);
                }
            })
        }
    };


</script>
    
<div class="h-dvh">

    {#if showGenerateProtocolDialog}
    <div class="relative z-10" aria-labelledby="modal-title" role="dialog" aria-modal="true">
        <!--
          Background backdrop, show/hide based on modal state.
      
          Entering: "ease-out duration-300"
            From: "opacity-0"
            To: "opacity-100"
          Leaving: "ease-in duration-200"
            From: "opacity-100"
            To: "opacity-0"
        -->
        <div class="fixed inset-0 bg-gray-500 bg-opacity-75 transition-opacity"></div>
      
        <div class="fixed inset-0 z-10 w-screen overflow-y-auto">
          <div class="flex min-h-full items-end justify-center p-4 text-center sm:items-center sm:p-0">
            <!--
              Modal panel, show/hide based on modal state.
      
              Entering: "ease-out duration-300"
                From: "opacity-0 translate-y-4 sm:translate-y-0 sm:scale-95"
                To: "opacity-100 translate-y-0 sm:scale-100"
              Leaving: "ease-in duration-200"
                From: "opacity-100 translate-y-0 sm:scale-100"
                To: "opacity-0 translate-y-4 sm:translate-y-0 sm:scale-95"
            -->
            <div class="relative transform overflow-hidden rounded-lg bg-white px-4 pb-4 pt-5 text-left shadow-xl transition-all sm:my-8 sm:w-full sm:max-w-lg sm:p-6">
            <div class="absolute right-0 top-0 hidden pr-4 pt-4 sm:block">
                <button type="button" class="rounded-md bg-white text-gray-400 hover:text-gray-500 focus:outline-none focus:ring-2 focus:ring-indigo-500 focus:ring-offset-2" on:click={() => {resetGenerateProtocol()}}>
                    <span class="sr-only">Close</span>
                    <svg class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" aria-hidden="true">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
                    </svg>
                </button>
              </div>
              <div>
                <div class="mt-3 sm:mt-5">
                  <h3 class="text-base font-semibold leading-6 text-gray-900" id="modal-title">Generate Lab Protocol</h3>
                  <div class="mt-2">
                    <p class="text-sm text-gray-500"></p>
                  </div>
                </div>
              </div>
              <div>
                <label for="comment" class="block text-sm font-medium leading-6 text-gray-900">Describe the protocol you'd like to generate in plain English. Provide as much detail as you can.</label>
                <div class="mt-2">
                  <textarea rows="4" name="comment" id="comment" class="block w-full rounded-md border-0 p-1.5 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-indigo-600 sm:text-sm sm:leading-6" bind:value={ generateProtocolPrompt }></textarea>
                </div>
              </div>
              <div class="mt-5 sm:mt-6 sm:grid sm:grid-flow-row-dense sm:grid-cols-2 sm:gap-3">
                <button type="button" class="inline-flex w-full justify-center rounded-md bg-indigo-600 px-3 py-2 text-sm font-semibold text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600 sm:col-start-2" on:click={() => generateProtocol()}>Go!</button>
              </div>
            </div>
          </div>
        </div>
      </div>
    {/if}
    
    <div class="flex flex-col">
        <div class="h-8 pt-2">
            <h1 class="pl-3 text-lg font-semibold">Untitled Protocol</h1>
        </div>
        <div class="grow">
            <Editor
            apiKey={ tinymceApiKey }
            conf={ tinymceConf }            
            bind:value={ protocol }
        />
        </div>        
    </div>
</div>

