1) Add the line:

	\Nette\Forms\Controls\CheckboxList::register();

   to app/bootstrap.php to register checkbox control.

2) Example of usage:

	$items = array(
	    1 => 'item1',
	    2 => 'item2',
	);
	
	$form = new \Nette\Application\UI\Form($this, 'checboxlistdemo');
	$form->addCheckboxList('demo', 'Choices', $items)
	    ->addRule('CheckboxList::validateChecked', 'Check something!');