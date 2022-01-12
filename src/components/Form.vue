<template>
<div>

      <FormulateForm v-model="formValues" :schema="schema" />
</div>
</template>

<script>
import '@/assets/formulate.css';

export default {
  name: 'formulate-form',
  data: () => {
    return {
      schema: [
          {
            "component": "h3",
            "children": "Hospital"
          },
          {
            "label": "Hospital name",
            "name": "name",
            "placeholder": "Hospital name",
            "validation": "required",
            "class": "form-control"
          },
          {
            "label": "Preferred abbreviation for the hospital",
            "name": " Abbreviation",
            "placeholder": "Preferred abbreviation for the hospital",
            "validation": "required"
          },
          {
            "component": 'div',
            "class": 'flex-wrapper',
            "children": [
              {
                "label": "Address line 1 (of the hospital)",
                "name": "address-1",
                "placeholder": "Address line 1 (of the hospital)",
              },
              {
                "label": "Address line 2 (of the hospital)",
                "name": "address-2",
                "placeholder": "Address line 2 (of the hospital)",
              },
              {
                "label": "City (of the hospital)",
                "name": "city",
                "placeholder": "City (of the hospital)",
              },
              {
                "type": "select",
                "label": "Country (of the hospital)",
                "name": "country",
                "options": {
                  "eeuu": "United States",
                  "spain": "Spain",
                  "canada": "Canada",
                  "mexico": "Mexico",
                  "italy": "Italy",
                },
                "placeholder": "--Select country (of the hospital)--",
                "validation": "required"
              },
              {
                "type": "select",
                "label": "State (of the hospital)",
                "name": "State",
                "options": {
                  "kansas": "Kansas",
                  "Barcelona": "Barcelona",
                  "ottawa": "Ottawa",
                  "puebla": "puebla",
                  "verona": "Verona",
                },
                "placeholder": "--Select State (of the hospital)--",
              },
              {
                "label": "County (of the hospital)",
                "name": "County",
                "placeholder": "County (of the hospital)",
              },
              {
                "label": "County subunit (of the hospital)",
                "name": "County Subunit",
                "placeholder": "County subunit (of the hospital)",
              },
            ],
          },
          {
            "type": "select",
            "label": "Time zone (of the hospital)",
            "name": "Time zone",
            "options": {
              "Arabia": "UTC +4",
              "Atlantic ": "UTC -3",
              "Brasília ": "UTC -3",
              "Singapore": "UTC +8",
              "Peru ": "UTC -5",
            },
            "placeholder": "--Select Time zone (of the hospital)--",
            "validation": "required"
          },
          {
            "component": 'div',
            "class": 'flex-wrapper',
            "children": [
              {
                "type": "select",
                "label": "Hospital type",
                "name": "Hospital type",
                "options": {
                  "first level": "First level",
                  "high complexity ": "High complexity",
                  "small ": "Small",
                },
                "placeholder": "--Select--",
                "validation": "required"
              },
              {
                "type": "select",
                "label": "Hospital funding",
                "name": "Hospital funding",
                "options": {
                  "private": "Private",
                  "partner ": "Partners",
                  "public": "Public",
                },
                "placeholder": "--Select--",
              },
            ]
          },
          {
            "type": 'textarea',
            "label": "Hospital comments",
            "name": "Hospital comments",
            "placeholder": "Hospital comments",
          },
      ],
      formValues: {}
    }
  },
}
</script>
