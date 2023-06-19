```javascript 
const formatAvailabilityDates = (availability) => {

	const moveInDate = `${availability?.move_in.start.day}/${availability?.move_in.start.month}-${availability?.move_in.end.day}/${availability?.move_in.end.month}`;
	
	const moveOutDate = `${availability?.move_out.start.day}/${availability?.move_out.start.month}-${availability?.move_out.end.day}/${availability?.move_out.end.month}`;

return { moveInDate, moveOutDate }

};
```

```javascript
const formatAvailabilityDates = (availability) => {

	const moveInStartDate = new Date(new Date().getFullYear(), availability?.move_in.start.month - 1,availability?.move_in.start.day);
	
	const moveInEndDate = new Date(new Date().getFullYear(), availability?.move_in.end.month - 1, availability?.move_in.end.d);
	
	const moveOutStartDate = new Date(new Date().getFullYear(), availability?.move_out.start.month - 1, availability?.move_out.start.day);
	
	const moveOutEndDate = new Date(new Date().getFullYear(), availability?.move_out.end.month - 1, availability?.move_out.end.day);
	
	  
	
	const options = options;
	
	const moveInDate = `${moveInStartDate.toLocaleString(locale, options)}-${moveInEndDate.toLocaleString(locale, options)}`;
	
	const moveOutDate = `${moveOutStartDate.toLocaleString(locale, options)}-${moveOutEndDate.toLocaleString(locale, options)}`;

  

return { moveInDate, moveOutDate };

};
```

```javascript
export const parseYearFromAvailabilitySlot = (slot) => {

	const currentYear = new Date().getFullYear();
	const currentMonth = new Date().getMonth() + 1;
	
	  
	const moveInStartMonth = slot.move_in.start.month;
	const moveInEndMonth = slot.move_in.end.month;
	const moveOutStartMonth = slot.move_out.start.month;
	const moveOutEndMonth = slot.move_out.end.month;
	
	  
	let moveInStartYear = currentYear;
	let moveInEndYear = currentYear;
	let moveOutStartYear = currentYear;
	let moveOutEndYear = currentYear;
	
	  
	if (moveInStartMonth < currentMonth) {
		moveInStartYear = currentYear + 1;
		moveInEndYear = currentYear + 1;
		moveOutStartYear = currentYear + 1;
		moveOutEndYear = currentYear + 1;
	}
	
	  
	
	if (moveInStartMonth > moveInEndMonth) {
		moveInEndYear = moveInStartYear + 1;
	} else if (moveOutStartMonth > moveOutEndMonth) {
		moveOutEndYear = moveOutStartYear + 1;
	}
	
	  
	
	if (moveOutStartMonth < moveInStartMonth || (moveOutStartMonth === moveInStartMonth && moveOutStartMonth < currentMonth)) {
		moveOutStartYear = moveInEndYear;
	
		if (moveOutStartMonth < moveInEndMonth) {
			moveOutStartYear = moveInEndYear + 1;
		}
	
		if (moveOutStartMonth > moveOutEndMonth) {
			moveOutEndYear = moveOutStartYear + 1;
		}
	
	}
	  
	if (moveInStartMonth === moveInEndMonth || moveOutStartMonth === moveOutEndMonth) {
		moveInEndYear = moveInStartYear;
		moveOutEndYear = moveOutStartYear;
	}
	
	return { 
		moveInStartYear, 
		moveInEndYear, 
		moveOutStartYear, 
		moveOutEndYear 
	};

};
```
