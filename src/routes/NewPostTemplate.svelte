<!-- src/routes/about.svelte -->
<script>
    import FormNormalInput from './FormNormalInput.svelte'
    import FormDropdownInput from './FormDropdownInput.svelte'
    import FormCheckBoxInput from './FormCheckBoxInput.svelte'
    import FormTextAreaInput from './FormTextAreaInput.svelte'
    let paymentOptions = [{label:"GCash", key:"gcash"}, {label:"PayMaya", key:"paymaya"}, {label:"Cebuana", key:"cebuana"}, {label:"Bank Transfer", key:"banktr"} ]
    let pricingTypes = [{label:"hourly", key:"hourly"}, {label:"daily", key:"daily"}, {label:"weekly", key:"weekly"}, {label:"monthly", key:"monthly"}, {label:"yearly", key:"yearly"} ]
</script>

<style>
.content {
  display: grid;
  grid-template-columns: 20% 80%;
  grid-column-gap: 10px;
}
</style>

<h1>Add a new Plant</h1>
<br>



<form class="w-full overflow-hidden lg:w-3/4 xl:w-3/4">
    <FormNormalInput labeltxt={"Post Title"} fieldid={"title"} inptype={"text"} placeholder={"A short title for this post"}  />
    <FormTextAreaInput labeltxt={"Description"} fieldid={"description"}  placeholder={"A detailed description of your product or service"}  />
    <FormDropdownInput labeltxt={"Accepted Payments"} fieldid={"paytypes"} fieldoptions={paymentOptions} placeholder={""}  />
    
    <div class="flex flex-row w-full overflow-hidden">
        <div class="w-full overflow-hidden lg:w-1/2 xl:w-1/2 bg-red">
            <FormNormalInput labeltxt={"Price"} fieldid={"addrno"} inptype={"text"}   />  
        </div>
        <div class="w-full overflow-hidden lg:w-1/2 xl:w-1/2 bg-green">
            <FormDropdownInput labeltxt={"Price type"} fieldid={"pricetypes"} fieldoptions={pricingTypes} placeholder={""}  />    
        </div>
        

        
        
        
    </div>
    
    <FormNormalInput labeltxt={"Building Number"} fieldid={"addrno"} inptype={"text"}   />  
    <FormNormalInput labeltxt={"Street Name"} fieldid={"addrstreet"} inptype={"text"}   />  
    <FormNormalInput labeltxt={"Barangay"} fieldid={"addrbarangay"} inptype={"text"}   />  
    <FormNormalInput labeltxt={"City"} fieldid={"addrcity"} inptype={"text"}   />  
    <FormNormalInput labeltxt={"Province"} fieldid={"addrprovince"} inptype={"text"}   />  
    <FormNormalInput labeltxt={"ZIP"} fieldid={"addrzip"} inptype={"text"}   />  
</form>

