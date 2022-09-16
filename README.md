# flutter_future_build

A new Flutter project. This prjoect is about FutureBuilder Widget. İt's too eays simple words now. Keep going learning Flutter!!!!

    Future<int>calculateFactorial (int number) async{
        int result =1;
        for (var i = 1; i <= number; i++) {
            result = result*i;}
            return result;}

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text(widget.title),),
      body: Center(
        child: Column(
          mainAxisAlignment: MainAxisAlignment.center,
          children: <Widget>[
                FutureBuilder<int>(
                  future: calculateFactorial(4), //this number key is userkey
                  builder: (context, snapshot) {
                    if (snapshot.hasError){print('ErrorResult : ${snapshot.error}');}
                    if (snapshot.hasData){return Text('IncludingData : ${snapshot.data}');}
                    else{return Text('NoData');}},
            ),

