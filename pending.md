1. Routering & Navigation
    ```tsx
    // app/movie/[id].tsx
    import { useLocalSearchParams } from "expo-router";
    import { StyleSheet, Text, View } from "react-native";

    const Details = () => {
        const { id } = useLocalSearchParams();
        return (
            <View>
                <Text>
                    Movie details: {id}
                </Text>
            </View>
        )
    }

    export default Details
    const styles = StyleSheet.create({})
    // --------------------------------------------
    // app/onboarding.tsx
    import { StyleSheet, Text, View } from "react-native";

    const onboarding = () => {
        return (
            <View>
                <Text>
                    Onboarding
                </Text>
            </View>
        )
    }

    export default onboarding
    const styles = StyleSheet.create({})
    // --------------------------------------------------
    // index.tsx
    import { Link } from "expo-router";
    import { Text, View } from "react-native";

    export default function Index() {
    return (
        <View className="flex-1 items-center justify-center">
        <Text className="text-5xl font-bold text-light-300">
            Welcome!
        </Text>
        <Link href='/onboarding'>Onboarding</Link>
        <Link href={{
            pathname: '/movie/[id]',
            params: { id: 'avengers' }
        }}>Avenger Movie</Link>

        </View>
    );
    }
    ```