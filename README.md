# Hide Fields Product Edit
Essa modificação tem o intuito de esconder os campos não utilizados no cadastro do produto.
Para tal o XML apenas aplica uma classe "hidden" junto a classe "form-group", assim escondendo a mesma do view.
O XML faz a contagem dos "form-group", caso queira alterar o numero, precisa editar o xml e mover o numero desejado.

# code

```
<?xml version="1.0" encoding="utf-8"?>
<modification>
	<name>Hide Fields Admin</name>
	<code>hide-filds-admin</code>
	<version>3.0</version>
	<author>REDS</author>
	<link>http://www.agenciaprai.com/</link>

	<file path="admin/view/template/catalog/product_form.twig">
			<operation>
				<search position="replace" index="5,6,7,8,9,10"><![CDATA[
					<div class="form-group">
				]]></search>
				<add><![CDATA[
				<div class="form-group hidden">
				]]></add>
			</operation>
	</file>
</modification>

´´´
