	;Paxton Proctor
			.model	small
			.stack	100h
			.data
	var		db		"This is an example of subtracting two numbers: 92 - 22 = $"
			.code
	main:	mov		ax,@data
			mov		ds,ax
			
			mov		ah,9
			lea		dx,var
			int		21h
			
			mov		cl, 92
			mov		bl, 22
			sub		cl, bl
			
			mov		dl, cl
			mov		ah, 2
			int		21h
			
			mov		ah, 4ch
			int		21h
			end		main
			