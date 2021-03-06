# yii2-widget-datetimepicker
This extension provides a `date`, `time` or `datetime` picker widget for yii2 framework in **Bootstrap 4** style. It's based 
on [Tempus Dominus](https://tempusdominus.github.io/bootstrap-4/).
 
## Resources
 * [yii2](https://github.com/yiisoft/yii2) framework
 * [Tempus Dominus](https://tempusdominus.github.io/bootstrap-4/)
 
## Installation

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
$ php composer.phar require --prefer-dist simialbi/yii2-widget-datetimepicker
```

or add 

```
"simialbi/yii2-widget-datetimepicker": "~2.0"
```

to the ```require``` section of your `composer.json`

## Example Usage

To include datepicker instance in one of your pages, call the widget like this:
```php
<?php
/* @var $this yii\web\View */
/* @var $model yii\base\Model */

use yii\widgets\ActiveForm;
use simialbi\yii2\date\Datetimepicker;

$this->title = 'myForm';
$this->params['breadcrumbs'][] = $this->title;

?>
<div class="my-form">
	<?php $form = ActiveForm::begin(['id' => 'my-form']); ?>
		<?= $form->field($model, 'name')->textInput(['autofocus' => true]) ?>
		<?= $form->field($model, 'birthday')->widget(Datetimepicker::class, [
				'format' => 'mm/dd/yyyy',
				'type'   => Datetimepicker::TYPE_COMPONENT_APPEND
			]) ?>
		<?= $form->field($model, 'email') ?>
	<?php ActiveForm::end(); ?>
</div>
```

## License

**yii2-widget-datetimepicker** is released under MIT license. See bundled [LICENSE](LICENSE) for details.