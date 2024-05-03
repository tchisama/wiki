


### Odoo XML Cheat Sheet

#### Basic Structure:
```xml
<?xml version="1.0" encoding="utf-8"?>
<odoo>
    <!-- Your XML code here -->
</odoo>
```
Explanation: This is the basic structure of an XML file for Odoo modules. It starts with the XML declaration (`<?xml version="1.0" encoding="utf-8"?>`) followed by the `<odoo>` root element. All Odoo XML code should be encapsulated within the `<odoo>` tags.

#### Modules:
- **Module Declaration:**
  ```xml
  <odoo>
      <data>
          <record id="module_name" model="ir.module.module">
              <field name="name">Module Name</field>
              <field name="description">Module Description</field>
              <field name="state">installed</field>
              <!-- Additional fields -->
          </record>
      </data>
  </odoo>
  ```
Explanation: This section defines a new module in Odoo. It uses the `ir.module.module` model to create a record for the module with specified attributes such as name, description, and state (usually installed).

#### Views:
- **Form View:**
  ```xml
  <record id="view_name" model="ir.ui.view">
      <field name="name">View Name</field>
      <field name="model">model.name</field>
      <field name="arch" type="xml">
          <!-- Form view structure -->
      </field>
  </record>
  ```
  
- **Tree View:**
  ```xml
  <record id="view_name" model="ir.ui.view">
      <field name="name">View Name</field>
      <field name="model">model.name</field>
      <field name="arch" type="xml">
          <!-- Tree view structure -->
      </field>
  </record>
  ```

Explanation: These sections define views in Odoo. Views are used to present data to users. The `ir.ui.view` model is used to create view records with specified attributes such as name, model (which model the view is associated with), and arch (the XML structure of the view).

#### Fields:
- **Char Field:**
  ```xml
  <field name="field_name" type="char"/>
  ```

- **Integer Field:**
  ```xml
  <field name="field_name" type="integer"/>
  ```

- **Boolean Field:**
  ```xml
  <field name="field_name" type="boolean"/>
  ```

- **Selection Field:**
  ```xml
  <field name="field_name" type="selection">
      <selection string="Label" name="value"/>
  </field>
  ```

- **Many2one Field:**
  ```xml
  <field name="field_name" type="many2one" comodel="related.model"/>
  ```

- **Many2many Field:**
  ```xml
  <field name="field_name" type="many2many" comodel="related.model"/>
  ```

Explanation: These sections define various field types in Odoo models. Fields are used to store data in the database. Each field has attributes such as name (the field name), type (the field type), and additional attributes depending on the field type.

#### Actions:
- **Server Action:**
  ```xml
  <record id="action_id" model="ir.actions.server">
      <field name="name">Action Name</field>
      <field name="model_id" ref="model_name"/>
      <field name="state">code</field>
      <field name="code">
          <!-- Python code -->
      </field>
  </record>
  ```

- **Client Action:**
  ```xml
  <record id="action_id" model="ir.actions.client">
      <field name="name">Action Name</field>
      <field name="tag">Action Tag</field>
      <field name="context">{"key": "value"}</field>
  </record>
  ```

Explanation: These sections define actions in Odoo. Actions are used to perform operations such as executing server-side code (Server Action) or client-side actions like opening a window or executing JavaScript code (Client Action).

#### Menus:
- **Menu Item:**
  ```xml
  <menuitem id="menu_id" name="Menu Name" parent="parent_menu_id"/>
  ```

Explanation: This section defines menu items in Odoo. Menu items are used to create navigation menus in the Odoo user interface. Each menu item has attributes such as id (unique identifier), name (display name), and parent (the parent menu item).

#### Reports:
- **Qweb Report:**
  ```xml
  <report id="report_id" model="model.name" string="Report Name">
      <template id="template_id" name="template_name">
          <!-- Report template structure -->
      </template>
  </report>
  ```

Explanation: This section defines reports in Odoo. Reports are used to generate printable documents or views based on data from Odoo models. Qweb is the templating engine used in Odoo for report generation.

#### Security:
- **Access Control List (ACL):**
  ```xml
  <record id="record_id" model="ir.model.access">
      <field name="name">Access Name</field>
      <field name="model_id" ref="model_name"/>
      <field name="group_id" ref="base.group_user"/>
      <field name="perm_read" eval="True"/>
      <field name="perm_write" eval="True"/>
      <field name="perm_create" eval="True"/>
      <field name="perm_unlink" eval="True"/>
  </record>
  ```

Explanation: This section defines access control rules in Odoo. Access rules are used to control user access to models and records in the database. Each access rule specifies permissions (read, write, create, unlink) for a specific user group.

#### Example XML for a Module:
```xml
<odoo>
    <data>
        <record id="library_module" model="ir.module.module">
            <field name="name">Library Management</field>
            <field name="description">Module for managing libraries</field>
            <field name="state">installed</field>
        </record>
        
        <record id="book_form_view" model="ir.ui.view">
            <field name="name">Book Form</field>
            <field name="model">library.book</field>
            <field name="arch" type="xml">
                <!-- Form view structure for books -->
            </field>
        </record>
        
        <record id="book_tree_view" model="ir.ui.view">
            <field name="name">Book Tree</field>
            <field name="model">library.book</field>
            <field name="arch" type="xml">
                <!-- Tree view structure for books -->
            </field>
        </record>
        
        <!-- Additional XML records for menus, actions, security, etc. -->
    </data>
</odoo>
```

Explanation: This example XML defines a module called "Library Management" with views for managing books. It includes records for the module
