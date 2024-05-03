




# creating tree view in odoo


## 1. Create a model

```python
from odoo import models, fields
class MyModel(models.Model):
    _name = 'my.model'
    _description = 'My Model'

    name = fields.Char(string='Name')
    description = fields.Text(string='Description')
    date = fields.Date(string='Date')
    active = fields.Boolean(string='Active', default=True)
```


## 2. Create a tree view

```xml
<odoo>
  <menuitem
    id="menu_my_model" 
    name="My Model" 
  />
  <menuitem 
    id="menu_my_model_tree" 
    name="My Model Tree" 
    parent="menu_my_model" 
    action="action_my_model_tree"
  /> 
</odoo>
```

## 3. Create an action

```xml
<odoo>





  // action to be performed
  <record id="action_my_model_tree" model="ir.actions.act_window">
    <field name="name">My Model Tree</field> // name of the action
    <field name="res_model">my.model</field> // model to be used
    <field name="view_mode">tree,form</field> // view model
    <field name="domain">[]</field>
    <field name="context">{}</field>
  </record>
  
</odoo>
```

### what is a record ? 
A row, also known as a record or tuple, is a single entry within a table. It contains data organized into columns, each representing a specific attribute or field of the entity represented by the table.


## 4. Create a tree view

```xml
<odoo>
  // view to be displayed 
  <record id="view_my_model_tree" model="ir.ui.view">
    <field name="name">my.model.tree</field>
    <field name="model">my.model</field>
    <field name="arch" type="xml">
      <tree>
        <field name="name"/>
        <field name="description"/>
        <field name="date"/>
        <field name="active"/>
      </tree>
    </field>
  </record>
  
</odoo>
```


## 5 add the form view 

```xml
<odoo>
  <record id="view_my_model_form" model="ir.ui.view">
    <field name="name">my.model.form</field>
    <field name="model">my.model</field>
    <field name="arch" type="xml">
      <form>
        <sheet>
        <div class="oe_title"> // this part is optional just for styling
          <label for="name"/>
          <h1>
            <field name="name"/>
          </h1>
        </div>
          <group>
            <field name="description"/>
            <field name="date"/>
            <field name="active"/>
          </group>
        </sheet>
      </form>
    </field>
  </record>
</odoo>
```






