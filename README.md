# MultiSelect
A Lightning Multi-Select Picklist.

To use, simply add as part of a form (or without if you'd like):

    <div class="slds-form-element">
        <label class="slds-form-element__label" for="my-multi-select">Multi Select!!</label>
        <div class="slds-form-element__control">
            <c:MultiSelect aura:id="my-multi-select" options="{!v.myOptions}" selectChange="{!c.handleSelectChangeEvent}" selectedItems="{!v.mySelectedItems}" />
        </div>
    </div>
    
The multiselect `options` are an array of type `SelectItem[]` and selectedItems is a comma delimited string (`String[]`).

The `handleSelectChangeEvent` method could look like this:

    //changes filter parameters
    handleSelectChangeEvent: function(component, event, helper) {
        var items = component.get("v.items");
        items = event.getParam("values");
        component.set("v.items", items);
    }
    
I hope you find this useful :).

What it looks like:
[Imgur](http://i.imgur.com/22RPF0k.gifv)


