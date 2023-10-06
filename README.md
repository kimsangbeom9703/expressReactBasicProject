# react + express 기본 
```
    frontend = react = js + swc
    backend  = nodejs = express
```
## 
```
    npm install
    npm run build
    npm run dev or npm run new_start
```

## backend 구조 및 흐름?
```
    request -> routers -> middlewares(인증?) 없으면 제외 -> Controllesr -> services -> models 
    
    컨트롤러에서 req , res 를제어 하여 (유효성체크?)
    service에서 데이터 가공 후
    model에서 db삽입.
    
    ex)
    1. router.get('/',authmiddlewares,testController.home)
    2. authmiddlewares 로그인 체크
    3. testController
        module.exports = {
            home:(req,res,next) => {
                const data = testService.getTest()
                res.json(data)             
            }
        }
    4. testService
        module.exports = {
            getTest:() => {
                데이터 가공
                user = testModel.get()
                return user
            }
        }    
    
    
```
