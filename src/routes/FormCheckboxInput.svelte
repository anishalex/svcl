<script>
    import { element, select_options } from "svelte/internal";
    
        export let labeltxt;
        export let fieldid;
        export let fieldoptions;
        export let placeholder;
    </script>
    
    <style>
        .content {
          display: grid;
          grid-template-columns: 20% 80%;
          grid-column-gap: 10px;
          
        }
    
        input:checked + div {
            @apply border-blue-500;
        }
        input:checked + div svg {
            @apply block;
        }
    </style>
    
    <div class="flex flex-col align-middle flex-wrap -mx-3 mb-6">
        <div class="relative items-center flex flex-row align-middle w-full md:w-full px-3 mb-6 md:mb-0">
          <label class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2" for={fieldid}>
          {labeltxt}
          </label>
          <input type="checkbox" id={fieldid} name={fieldid} value="no" class="opacity-0 absolute h-8 w-8" />
          <div class="bg-white border-2 rounded-md border-blue-400 w-8 h-8 flex flex-shrink-0 justify-center items-center mr-2 focus-within:border-blue-500">
            <svg class="fill-current hidden w-3 h-3 text-blue-600 pointer-events-none" version="1.1" viewBox="0 0 17 12" xmlns="http://www.w3.org/2000/svg">
              <g fill="#1F73F1" fill-rule="evenodd">
                <g transform="translate(-9 -11)" fill="#1F73F1" fill-rule="nonzero">
                  <path d="m25.576 11.414c0.56558 0.55188 0.56558 1.4439 0 1.9961l-9.404 9.176c-0.28213 0.27529-0.65247 0.41385-1.0228 0.41385-0.37034 0-0.74068-0.13855-1.0228-0.41385l-4.7019-4.588c-0.56584-0.55188-0.56584-1.4442 0-1.9961 0.56558-0.55214 1.4798-0.55214 2.0456 0l3.679 3.5899 8.3812-8.1779c0.56558-0.55214 1.4798-0.55214 2.0456 0z" />
                </g>
              </g>
            </svg>
          </div>      
        </div>
    </div>   