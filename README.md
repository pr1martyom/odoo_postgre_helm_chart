```
#Step 1: download git repository
1. git clone https://github.com/pr1martyom/odoo_postgre_helm_chart.git odoo_postgre_helm_chart

2. cd odoo_postgre_helm_chart

3. helm upgrade --install odoo -f values.yaml --set odoo.name=odoo2 --set odoo.label=odoo2 --set odoo.pvc.odooData.name=odoo-data2 --set odoo.pvc.odooAddons.name=odoo-addons2 --set postgres.name=db --set postgres.label=db --set postgres.pvc.name=postgre-data --set odoo.ingress.host=testci2.qzhub.net .

instruction:
--set odoo.name=odoo2 # name of odoo

--set odoo.label=odoo2 # label of odoo deployment

--set odoo.pvc.odooData.name=odoo-data2 # name of odoo pvc for data

--set odoo.pvc.odooAddons.name=odoo-addons2 # name of odoo pvc for addons

--set postgres.name=db. # name of postgres deployment

--set postgres.pvc.name=postgre-data # name of postgres pvc 

--set odoo.ingress.host=testci2.qzhub.net # domain name for ingress

--set odoo.args={"--init=website\,base\, etc."} 
```
