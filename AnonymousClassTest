package LamdaExpression;

/**
 * Created by Paritosh Dave on 9/21/2015.
 */
public class AnonymousClassTest {

    public static void main(String[] args) {
        int input1 = 100;
        int input2 = 10;

        // Non Lamda Code Usages .. using Anonymous class features
        MathOperation operation = new PerformMathOperation().getMathOperator();

        System.out.println("Max is: " + operation.max(input1, input2));
        System.out.println("Min is: " + operation.min(input1, input2));
        System.out.println("Add is: " + operation.add(input1, input2));
        System.out.println("Sub is: " + operation.sub(input1, input2));
        System.out.println("Multiplication is: " + operation.multiply(input1, input2));
        System.out.println("Division is: " + operation.divide(input1, input2));
    }

}

    interface MathOperation<Integer> {
        Integer max(Integer obj1, Integer obj2);

        Integer min(Integer obj1, Integer obj2);

        Integer add(Integer obj1, Integer obj2);

        Integer sub(Integer obj1, Integer obj2);

        Integer multiply(Integer obj1, Integer obj2);

        Integer divide(Integer obj1, Integer obj2);
    }

    class PerformMathOperation {
        public MathOperation getMathOperator() {
            MathOperation<Integer> mathOperationImplementation = new MathOperation<Integer>() {
                @Override
                public Integer max(Integer obj1, Integer obj2) {
                    return obj1 > obj2 ? obj1 : obj2;
                }

                @Override
                public Integer min(Integer obj1, Integer obj2) {
                    return obj1 > obj2 ? obj2 : obj1;
                }

                @Override
                public Integer add(Integer obj1, Integer obj2) {
                    return obj1 + obj2;
                }

                @Override
                public Integer sub(Integer obj1, Integer obj2) {
                    return obj1 - obj2;
                }

                @Override
                public Integer multiply(Integer obj1, Integer obj2) {
                    return obj1 * obj2;
                }

                @Override
                public Integer divide(Integer obj1, Integer obj2) {
                    if (obj2 != 0) return obj1 / obj2;
                    else throw new RuntimeException("Division not possible");
                }
            };
            return mathOperationImplementation;
        }
    }
