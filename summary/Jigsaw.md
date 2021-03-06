## Java Module Jigsaw

### Primary goals

> 1. 큰 애플리케이션이나 라이브러리를 개발자들이 쉽게 구조화 하거나 유지보수 할 수 있게 한다.
> 2. Java SE Platform 구현체와 JDK 의 보안과 유지보수성을 향상시킨다.
> 3. 애플리케이션 성능을 향상시킨다.
> 4. 소형 디바이스나 클라우드 개발에서 Java SE Platform, JDK 를 축소시켜 사용할 수 있도록 한다.
> <br>[OpenJDK 참조](https://openjdk.java.net/projects/jigsaw/)

### 설명

실제 프로젝트를 진행하면서 Java 모듈에 관련된 기술을 사용할 지는 의문이다. 여러 서비스에 사용할 모듈을
만들기는 하지만 그 규모자체가 크지 않기 때문에 필요한 API 만 오픈한다는 특징이 직접적으로 느껴지지는 않는다.
모듈을 만들때 접근제한자가 굉장히 중요하다는 사실은 최근 프로젝트를 진행하며 느끼고 있었다.
모듈을 사용하는 서비스에서 사용될 API 들만 명시적으로 지정하는 방법은 꽤 효과적일 것 같다.
모듈의 인터페이스를 통한 접근이 가장 올바르게 사용한다고 생각되지만 이전에는 이를 강제할 수 없었다.
만약 모듈을 도입한다면 특정 인터페이스만 사용할 수 있도록 사용자들에게 강제할 수 있고 이를 통해 확장성이
향상 될 것이라고 본다. 이런면에서 볼 때 보안이나 유지보수성이 높아 질 수 있을 것이라고 생각한다.    
