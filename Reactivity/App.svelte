<script>
	let count = 1

	$: doubled = count * 2
ㅁㄴㅇㄹ

	$: if(count >= 10){
		alert('10을 넘었습니다')
		count = 9
	}

	$: {
		console.log( count )
		console.log( doubled )
		
	}

	function handleClick() {
		count += 1
	}
</script>

<button on:click={handleClick}>
	클릭수 { count } { count === 1 ? 'time' : 'times'}
</button>

<p>{ count } 두배는 { doubled }</p>