https://dev.to/jahid6597/unleashing-the-quirky-and-weird-a-dive-into-the-world-of-javascript-22al

        function call_time_count(abc) { let a = 0; return (() => { return (abc = a++); }); }
        let call_count = call_time_count();
        for (let i = 0; i < 101; i++) {
            if (i % 5 === 0) {
                console.log("Number:", i, " time: ", call_count());
            }
        }


        function outer(abc) {
            let count = 0;
            function inner() {
                return (abc = count++);
            }
            return inner;
        }


        const closureFunc = outer();
        console.log(closureFunc());
        console.log(closureFunc());
        console.log(closureFunc());
        console.log(closureFunc());

